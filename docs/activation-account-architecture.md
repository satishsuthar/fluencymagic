# Fluency Activation Account Architecture

## Product Requirement

The 7-Day Fluency Activation Plan should behave like a mini web app, not a static page or PDF.

After the Free Fluency Test and lead capture, the system should automatically create a lightweight user profile. The MVP should avoid password signup and use magic-link or secure unique access links.

## Current Static MVP

The current implementation creates a lightweight activation profile in `localStorage` after the result page is viewed.

It supports:

- `/activation` dashboard
- `/activation/day-1` through `/activation/day-7`
- `/login`
- Current day tracking
- Completed day tracking
- Daily speaking task pages
- Browser recording metadata and local playback URL
- Reminder preference capture
- Day 1 versus Day 7 comparison surface
- CTA to the 30-Day Fluency Magic Challenge

Limitations:

- Profile is stored in the visitor's browser only.
- Access links are local prototype links, not real server-verified magic links.
- Recordings are not stored across devices.
- Email/WhatsApp reminders are preference-only until a backend is added.

## Production Serverless Architecture

Recommended AWS serverless architecture:

- CloudFront + S3 for static frontend.
- API Gateway HTTP API for activation endpoints.
- Lambda for profile creation, magic-link verification, progress updates, and reminder preferences.
- DynamoDB tables:
  - `FluencyMagicUsers`
  - `FluencyMagicActivationProgress`
  - `FluencyMagicMagicLinks`
- S3 private bucket prefix for user recordings if server-side recording storage is enabled.
- SES for email magic links and reminders.
- WhatsApp provider integration through a webhook Lambda, such as Twilio or Meta WhatsApp Cloud API.
- EventBridge Scheduler for daily reminders.

No IAM users or long-lived access keys are needed. Lambda roles should use least-privilege permissions.

## API Shape

### Create Activation Profile

`POST /activation/profile`

Input:

```json
{
  "lead": {
    "firstName": "Satish",
    "email": "satish@example.com",
    "phone": "+61..."
  },
  "testResult": {},
  "recommendedPlan": "wordAvailability"
}
```

Output:

```json
{
  "userId": "usr_...",
  "activationId": "act_...",
  "accessToken": "one-time-or-rotating-token",
  "activationUrl": "https://.../activation?token=..."
}
```

### Request Magic Link

`POST /login/magic-link`

Input:

```json
{
  "identifier": "satish@example.com"
}
```

Output:

```json
{
  "ok": true,
  "message": "If this profile exists, we sent your access link."
}
```

### Get Activation Dashboard

`GET /activation/profile?token=...`

Returns user profile, plan, completed days, current day, and recording metadata.

### Complete Day

`POST /activation/day/{day}/complete`

Stores completion and advances current day.

### Upload Daily Recording

Use pre-signed S3 upload URLs:

`POST /activation/day/{day}/recording-url`

Then browser uploads directly to S3.

### Reminder Preferences

`POST /activation/reminders`

Stores email/WhatsApp preferences and preferred time.

## Reminder Logic

For each active activation:

- If day not completed by reminder time, send reminder.
- If Day 7 completed, stop daily reminders and show 30-Day Challenge CTA.
- If user opts out, stop reminders immediately.

## Security Notes

- Magic-link tokens should expire.
- Store only hashed tokens in DynamoDB.
- Use one-time token exchange for a short-lived session token.
- Do not expose recordings publicly.
- Use signed URLs for uploads/downloads.
- Keep all messaging opt-in and unsubscribe-friendly.
