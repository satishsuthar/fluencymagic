# Free Fluency Test Product Specification

## User Flow

Landing page (`/`) -> Free Fluency Test (`/fluency-test`) -> profile questions -> speaking tasks -> lead capture -> result (`/fluency-test/result`) -> 7-Day Fluency Activation Plan (`/7-day-plan`).

The test is a focused mini web application, not a homepage section or popup. It uses one question per screen, a progress bar, recording screens, lead capture before the full report, and a personalised next step.

## Screen Copy

### Test Intro

Headline: Find Out Why You Get Stuck While Speaking English

Subheadline: You may understand English. You may know the words. But if your voice freezes when it is time to speak, your fluency system needs training. This free test will show where you are getting stuck and what to practise next.

Bullets:
- Discover your current fluency level
- Identify your biggest speaking block
- Understand whether your issue is word flow, sentence formation, grammar patterns, confidence, or expression
- Get your personalised 7-day practice direction

CTA: Start My Free Test

Microcopy: Takes around 3-5 minutes. No grammar exam. No judgement. Just a simple speaking diagnosis.

### Lead Capture

Headline: Your Fluency Report Is Ready

Subheadline: Enter your details to receive your fluency level, speaking block diagnosis, and personalised 7-day practice direction.

Fields: first name, email, WhatsApp number, country, main goal.

Button: Show My Fluency Report

Trust microcopy: We'll send your practice plan and reminders. No spam.

## Questions

1. What best describes you?
Options: Student, Job seeker, Working professional, Business owner, Homemaker, Migrant / living abroad, Other.

2. What is your biggest English speaking problem?
Options: I understand English but cannot speak fluently, I translate in my mind before speaking, I cannot find the right words quickly, I worry about grammar while speaking, My pronunciation or voice feels unclear, I feel nervous or embarrassed, I can speak but I do not sound natural.

3. Where do you need English the most?
Options: Job interviews, Workplace meetings, Client calls, Study / college, Social conversations, Travel / daily life, Presentations, General confidence.

4. How confident do you feel while speaking English?
Scale: 1 = Very nervous, 2 = Hesitant, 3 = Sometimes okay, 4 = Mostly confident, 5 = Very confident.

5. What usually happens when you try to speak English?
Options: I stop after a few words, I speak slowly with many pauses, I use very simple sentences, I make grammar mistakes and lose confidence, I forget words, I avoid speaking, I can speak but I do not sound polished.

6. How often do you practise speaking English aloud?
Options: Almost never, Once or twice a week, A few minutes daily, Regularly, I speak often but still want to improve.

7. What is your main goal?
Options: Speak without hesitation, Improve interview confidence, Speak better at work, Sound more natural, Improve pronunciation and clarity, Build daily speaking habit, Express thoughts clearly.

## Speaking Tasks

### Main 60-Second Speaking Task

Instruction: Now speak for 60 seconds. Do not worry about perfect grammar. Just speak naturally.

Prompt: Tell us about yourself, where you use English, and what problem you face when you try to speak.

Support prompts: Who are you? Where do you need English? What happens when you try to speak? What do you want to improve? How would your life change if you spoke English confidently?

### Word Flow Check

Instruction: Use the word "confidence" in three different spoken sentences.

Evaluation: natural use, related forms, meaningful sentences, natural word groups, struggle level.

### Sentence Pattern Check

Instruction: Complete and speak these sentence starters naturally.

Starters:
- I want to improve...
- I have been trying to...
- One challenge I face is...
- I feel more confident when...

Evaluation: completion, grammar pattern comfort, natural flow, idea expansion, hesitation.

### Real-Life Speaking Check

Prompt: Imagine you are in a job interview or professional introduction. Answer: "Tell me about yourself."

Evaluation: clarity, organisation, confidence, sentence flow, natural expression, filler words.

## Scoring Criteria

Each area is scored 0-100:

- Speech Flow: smoothness, pauses, hesitation, rhythm, ability to continue.
- Word Availability: finding words quickly, useful vocabulary, natural word combinations, common-word flexibility.
- Sentence Pattern Comfort: complete sentences, natural grammar patterns, sentence expansion, reduced grammar confusion.
- Expression Clarity: clear ideas, explanation, organisation, meaningful communication.
- Naturalness: natural sentence quality, common expressions, less translation-style English, conversational quality.
- Speaking Confidence: voice steadiness, willingness to continue, energy, self-assurance, reduced nervousness.

Overall Fluency Score: average of all six areas.

Current static implementation uses self-assessment, practice frequency, and recording completion as a lightweight heuristic. Production should replace or enrich this with transcript-based analysis.

## Fluency Levels

Level 1: Silent Understander, 0-25. Speaking feels uncomfortable. Focus on mouth movement, simple sentence flow, and basic confidence.

Level 2: Hesitant Speaker, 26-45. User can speak some English but pauses, translates, searches for words, or worries about grammar. Focus on speech flow, word combinations, and daily speaking practice.

Level 3: Functional Speaker, 46-65. User can communicate basic ideas, but speech may feel slow, simple, or unnatural. Focus on sentence patterns, word groups, and expression practice.

Level 4: Natural Speaker, 66-82. User speaks clearly in many situations but needs polish, confidence, expression, and professional fluency.

Level 5: Confident Communicator, 83-100. User speaks with clarity, flow, and confidence. Focus on advanced expression, storytelling, professional presence, and powerful communication.

## Speaking Block Logic

Mouth Flow Block: user knows what to say, but the mouth does not move smoothly. Practice: speech organ drills, rhythm practice, repeated phrase speaking.

Word Availability Block: words are understood but not ready in useful groups. Practice: word combination drills, core word command, phrase groups.

Sentence Formation Block: words are known, but sentences do not form naturally. Practice: sentence pattern gym, sentence expansion drills.

Grammar Pattern Block: correctness checking breaks flow. Practice: pattern-based grammar and repeated natural sentence structures.

Expression Block: basic English works, but real thoughts and personality do not come out. Practice: expression upgrade drills, storytelling, real-life tasks.

Confidence Block: nervousness stops flow. Practice: daily speaking missions, safe recording practice, confidence-building repetition.

## 7-Day Plan Logic

Mouth Flow Block:
Day 1 short phrase repetition; Day 2 mouth movement sentence expansion; Day 3 slow-clear-fast speaking drill; Day 4 rhythm and breath; Day 5 60-second speaking; Day 6 re-record and compare; Day 7 fluency flow review.

Word Availability Block:
Day 1 confidence; Day 2 problem; Day 3 improve; Day 4 work; Day 5 word group speaking; Day 6 sentence creation from word groups; Day 7 personal speaking task.

Sentence Formation Block:
Day 1 I want to; Day 2 I have been trying to; Day 3 One challenge I face is; Day 4 The reason is; Day 5 What I mean is; Day 6 Let me explain; Day 7 60-second pattern speaking.

Grammar Pattern Block:
Day 1 I am / I have / I want patterns; Day 2 past experience; Day 3 future plan; Day 4 opinion; Day 5 question; Day 6 correction without rule memorisation; Day 7 natural speaking review.

Expression Block:
Day 1 feelings; Day 2 opinions; Day 3 problems; Day 4 workplace; Day 5 storytelling; Day 6 personal introduction upgrade; Day 7 real conversation practice.

Confidence Block:
Day 1 safe 30-second speaking; Day 2 speak slowly and clearly; Day 3 record without deleting; Day 4 speak about yourself; Day 5 speak about your goal; Day 6 repeat and improve; Day 7 confidence review.

## UI/UX Notes

The experience should be mobile-first, premium, calm, motivational, and non-exam-like. Use one question per screen, a clear progress bar, encouraging microcopy, simple recording buttons, timer, score cards, level badge, block diagnosis card, and strong next-step CTAs. Avoid red error styling for performance. Use warm guidance instead.

## Technical Notes

Current implementation is static and stores test state in `localStorage`. Browser recording uses `MediaRecorder` when microphone permission is available. The app first attempts live browser speech recognition during recording, then falls back to Transformers.js with a small Whisper model that decodes the recording locally. The transcript is shown to the user and transcript heuristics improve the scoring. If microphone access, model loading, or transcription fails, users can continue in practice mode and still receive a preliminary self-assessment-based result.

Production implementation should add:
- Secure API endpoint for lead capture and consent if leads should be saved.
- Optional secure object storage upload for audio files only if users consent to server-side analysis.
- Server-side transcription job only if browser-local transcription is not enough for production quality.
- Stronger transcript-based scoring for hesitation markers, sentence completeness, word choice, word-combination quality, clarity, naturalness, and ability to continue.
- Optional tone/confidence scoring only if reliable and consented.
- Analytics events for route view, question answered, recording completed, lead submitted, result viewed, and plan CTA clicked.

## Data Fields

Store: first name, email, phone / WhatsApp, country, user category, main goal, self-reported problem, confidence rating, practice frequency, speaking context, what happens when speaking, voice recording files, transcription, six area scores, overall score, fluency level, main speaking block, recommended plan, date/time of test, consent and source page.

## Conversion Copy

Headline: Your Fluency Can Improve Faster When You Practise the Right Way

Copy: Most people keep watching English videos, memorising words, or waiting for confidence. But speaking improves when you practise the right word groups, sentence patterns, and voice flow every day.

Your report shows where your fluency is getting stuck. The 7-Day Fluency Activation Plan gives you your first set of guided speaking drills to start building flow.

CTA: Start My Free 7-Day Plan

## Edge Cases And Fallbacks

- Microphone blocked: allow practice mode and explain that the report will be based on self-assessment until recording is available.
- User exits mid-test: preserve answers in local storage in a future iteration.
- No result state on result page: show a friendly prompt to start the test.
- No plan key: default to Word Availability Block.
- Unsupported browser recording: continue with self-assessment and clearly label recording as unavailable.
- Slow network or upload failure in production: save local progress, retry upload, and let the user continue when possible.
- Empty or very short audio in production: ask user to retry once with supportive copy.
