# 7-Day Fluency Activation Mini-App Specification

## 1. Product Purpose

The 7-Day Fluency Activation Mini-App helps users experience the Fluency Magic method after they complete the Free Fluency Test.

It is not a PDF, static content page, or word-list plan. It is a focused, mobile-first speaking practice app that helps users train their voice, word flow, sentence patterns, expression, and confidence for seven days.

The goal is not to make the user fully fluent in seven days. The goal is to create belief:

> For the first time, I understand how to practise speaking properly.

## 2. User Journey

Landing Page -> Free Fluency Test -> Lead Capture -> Fluency Result -> Recommended 7-Day Fluency Activation -> Activation Dashboard -> Daily Practice -> Day 7 Review -> 30-Day Fluency Magic Challenge.

The 7-day mini-app should create:

- trust through a personalised plan
- momentum through daily completion
- visible progress through recordings and reflections
- conversion desire through before/after comparison

## 3. Routes And Pages

Required routes:

- `/activation` main 7-day dashboard
- `/activation/day-1`
- `/activation/day-2`
- `/activation/day-3`
- `/activation/day-4`
- `/activation/day-5`
- `/activation/day-6`
- `/activation/day-7`
- `/login` magic link or access-link entry

The activation experience is separate from the landing page and should feel like a lightweight app.

## 4. Account And Access Flow

After the Free Fluency Test lead capture, automatically create a lightweight user profile.

MVP access options:

- secure token-based personal access link
- email magic link
- WhatsApp access link later

No password is required for MVP.

Access paths:

- result page CTA
- email reminder link
- WhatsApp reminder link
- `/login`

MVP static prototype can store the activation profile locally. Production must store it server-side so users can return across devices.

## 5. Dashboard Copy And Layout

Route: `/activation`

Dashboard sections:

### Greeting

Copy:

Welcome back, [First Name].

### Headline

Your 7-Day Fluency Activation

### Subheadline

Each day gives you a short speaking practice session to train your voice, word flow, sentence patterns, and confidence.

### User Result Summary

Show:

- Your level: Level 2 - Hesitant Speaker
- Main focus: Word Availability Block
- Today is Day 2 of your 7-Day Fluency Activation
- Today's focus: Make Words Come Faster

### Progress Path

Show Day 1 to Day 7:

- Day 1 complete
- Day 2 unlocked
- Day 3 locked
- Day 4 locked
- Day 5 locked
- Day 6 locked
- Day 7 locked

Use icons visually, but avoid school-like grading.

### Streak

Copy:

Current streak: 1 day

### Primary CTA

Start Today's Practice

### Secondary Actions

- View my fluency result
- Retake fluency test
- Contact support

### Motivational Line

You do not become fluent by waiting. You become fluent by speaking - one day at a time.

## 6. Daily Practice Structure

Each day follows the same app-like flow:

1. Today's Focus
2. Voice Flow Drill
3. Word Combination Drill
4. Sentence Pattern Drill
5. Say It Better Drill
6. Speaking Mission
7. Reflection
8. Complete Day

Each session should take around 7-12 minutes.

The user should tap through sections, record the speaking mission, answer one reflection, and mark the day complete.

## 7. Daily Screen UI

Header:

Day X of 7

Progress:

Day 2 / 7

Theme:

Make Words Come Faster

Estimated time:

7-12 minutes

Cards:

- Voice Flow
- Word Combinations
- Sentence Patterns
- Say It Better
- Speaking Mission
- Reflection

Recording UI:

- Record button
- Stop button
- Timer
- Re-record option
- Save recording
- Use this recording

Completion UI:

- Mark Day Complete
- Continue Tomorrow
- Back to Dashboard

Tone:

Warm, supportive, non-judgemental.

## 8. Full Day Content

### Day 1: Start Speaking Without Freezing

Purpose:

Activate the user's voice and reduce fear of speaking.

Today's Focus:

Today you will start speaking slowly and clearly without judging yourself. The goal is not perfect English. The goal is to begin.

Voice Flow Drill:

Say each line slowly three times:

- I can speak.
- I can speak slowly.
- I can speak slowly and clearly.
- I can speak slowly and clearly without rushing.
- I can speak slowly and clearly without judging myself.

Word Combination Drill:

Core word: confidence

Practise aloud:

- build confidence
- gain confidence
- lose confidence
- speak with confidence
- confidence in myself
- more confident
- confident speaker
- speak confidently

Practice sentences:

- I want to build confidence in English.
- I lose confidence when I cannot find the right words.
- Daily speaking practice helps me become more confident.
- I want to speak confidently in real conversations.

Sentence Pattern Drill:

- I want to improve...
- I feel nervous when...
- I lose confidence when...
- I feel more confident when...
- I am learning to...

Say It Better Drill:

Basic sentence:

My English is weak.

Better versions:

- I am still building my English fluency.
- I understand English, but I need more speaking practice.
- I want to become more natural and confident in English.
- My speaking is improving step by step.

Speaking Mission:

Record a 45-second answer:

Why do you want to improve your English speaking?

Support prompts:

- Where do you need English?
- What happens when you try to speak?
- How do you want to feel when speaking English?

Reflection:

What felt easier today: starting the sentence, finding words, or speaking aloud?

Completion message:

Day 1 complete. You have started training your voice. That is the first real step.

### Day 2: Make Words Come Faster

Purpose:

Help users understand that fluency comes from ready word groups, not isolated words.

Today's Focus:

Today you will practise useful word combinations so words come faster when you speak.

Voice Flow Drill:

- Words can come.
- Words can come faster.
- Useful words can come faster.
- Useful words can come faster when I practise them in groups.
- Useful words can come faster when I practise them in real sentences.

Word Combination Drill:

Core word: problem

- face a problem
- solve a problem
- create a problem
- avoid a problem
- serious problem
- common problem
- main problem
- problem with communication

Practice sentences:

- I face this problem when I try to speak English.
- The main problem is that I translate in my mind.
- I want to solve this problem through daily practice.
- Lack of speaking practice creates this problem.

Sentence Pattern Drill:

- The main problem is...
- I face this problem when...
- I want to solve...
- One common problem is...
- This becomes difficult because...

Say It Better Drill:

Basic sentence:

I don't get words.

Better versions:

- I cannot find the right words quickly.
- The words do not come fast enough when I speak.
- I know the words, but they are not ready when I need them.
- I need to practise useful word groups so I can speak faster.

Speaking Mission:

Record a 45-60 second answer:

What is the biggest problem you face while speaking English?

Reflection:

Which word group felt most useful today?

Completion message:

Day 2 complete. Today you trained words in groups, not as isolated vocabulary.

### Day 3: Form Sentences Naturally

Purpose:

Help users practise sentence patterns so grammar becomes automatic.

Today's Focus:

Today you will practise natural sentence patterns so complete sentences come more easily.

Voice Flow Drill:

- I can form sentences.
- I can form simple sentences.
- I can form simple sentences clearly.
- I can form simple sentences clearly with practice.
- I can form simple sentences clearly without overthinking grammar.

Word Combination Drill:

Core word: improve

- improve my English
- improve my speaking
- improve my confidence
- improve my pronunciation
- improve step by step
- improve through practice
- improve my communication
- improve every day

Sentence Pattern Drill:

- I want to improve...
- I am trying to improve...
- I have been trying to improve...
- I can improve by...
- I will improve if...

Say It Better Drill:

Basic sentence:

I want good English.

Better versions:

- I want to improve my spoken English.
- I want to speak English more clearly and confidently.
- I want to express my thoughts naturally in English.
- I want to build real fluency through daily practice.

Speaking Mission:

Record a 60-second answer:

What exactly do you want to improve in your English speaking?

Reflection:

Which sentence pattern helped you speak most easily today?

Completion message:

Day 3 complete. You are now training sentence patterns instead of memorising grammar rules.

Light conversion line:

You have now practised voice flow, word groups, and sentence patterns. These are the foundations of real fluency.

### Day 4: Stop Translating In Your Head

Purpose:

Help users practise direct English thinking through repeated patterns and simple idea flow.

Today's Focus:

Today you will practise speaking directly in English without translating every word in your mind.

Voice Flow Drill:

- I can think in English.
- I can think in simple English.
- I can speak in simple English.
- I can express one idea at a time.
- I can express one idea at a time without translating everything.

Word Combination Drill:

Core word: idea

- express an idea
- share an idea
- explain an idea
- clear idea
- simple idea
- main idea
- better idea
- idea in my mind

Sentence Pattern Drill:

- I think...
- I feel...
- I believe...
- In my opinion...
- The main idea is...
- What I mean is...

Say It Better Drill:

Basic sentence:

I have thoughts but I cannot say.

Better versions:

- I have thoughts, but I find it difficult to express them in English.
- I know what I want to say, but I get stuck while speaking.
- My ideas are clear in my mind, but they do not come out smoothly.
- I want to express my ideas clearly and naturally.

Speaking Mission:

Record a 60-second answer:

Share one opinion about learning English.

Reflection:

Did speaking one idea at a time feel easier than translating full sentences?

Completion message:

Day 4 complete. Today you practised expressing ideas directly in English.

### Day 5: Say Simple Things Better

Purpose:

Help users upgrade basic English into natural, expressive English.

Today's Focus:

Today you will practise saying simple thoughts in a more natural and confident way.

Voice Flow Drill:

- I can say it better.
- I can say simple things better.
- I can express simple thoughts better.
- I can express simple thoughts better with natural English.
- I can express simple thoughts better with practice and confidence.

Word Combination Drill:

Core word: feel

- feel nervous
- feel confident
- feel comfortable
- feel stuck
- feel ready
- feel proud
- feel better
- feel natural

Sentence Pattern Drill:

- I feel nervous when...
- I feel confident when...
- I feel comfortable with...
- I feel stuck because...
- I feel proud when...

Say It Better Drill:

Basic sentence:

I am afraid to speak English.

Better versions:

- I feel nervous when I have to speak English.
- I hesitate because I worry about making mistakes.
- I want to become more comfortable speaking English.
- I am learning to speak with more confidence.

Speaking Mission:

Record a 60-second answer:

How do you feel when you have to speak English, and how do you want to feel instead?

Reflection:

Which better sentence sounded most natural to you?

Completion message:

Day 5 complete. Today you practised expressing feelings more naturally.

Light conversion line:

You are starting to see how simple English can become more natural with the right practice.

### Day 6: Speak In A Real Situation

Purpose:

Apply practice to a realistic speaking situation.

Today's Focus:

Today you will practise speaking in a real-life situation so your English becomes useful, not theoretical.

Voice Flow Drill:

- I can handle a conversation.
- I can handle a simple conversation.
- I can handle a simple conversation in English.
- I can handle a simple conversation in English one sentence at a time.
- I can handle a simple conversation in English with calm confidence.

Word Combination Drill:

Core word: work

- work on my English
- work on my confidence
- work with people
- work in a team
- work under pressure
- work experience
- workplace communication
- work-related conversation

Sentence Pattern Drill:

- I am currently working on...
- I have experience in...
- I usually work with...
- At work, I need to...
- I want to become better at...

Say It Better Drill:

Basic sentence:

I need English for job.

Better versions:

- I need English for my career growth.
- I want to speak more confidently at work.
- I need English for interviews, meetings, and professional conversations.
- Better English will help me express myself more clearly at work.

Speaking Mission:

Choose one situation and record a 60-second response:

- Introduce yourself professionally.
- Explain your current work or study.
- Talk about why English is important for your career.

Reflection:

Which situation felt most useful for your real life?

Completion message:

Day 6 complete. Today you practised English for a real situation, not just for learning.

### Day 7: Review Your Progress

Purpose:

Help users compare Day 1 and Day 7, feel progress, and move toward the paid challenge.

Today's Focus:

Today you will record again, compare your progress, and see what continued practice can do.

Voice Flow Drill:

- I have started.
- I have practised for seven days.
- I have trained my voice for seven days.
- I have trained my voice, words, patterns, and confidence.
- I can continue improving with daily speaking practice.

Word Combination Drill:

Core word: progress

- make progress
- see progress
- small progress
- steady progress
- real progress
- progress through practice
- progress every day
- continue my progress

Sentence Pattern Drill:

- In the last seven days, I have...
- I noticed that...
- I feel more comfortable with...
- I still want to improve...
- My next goal is...

Say It Better Drill:

Basic sentence:

I improved little.

Better versions:

- I have started making progress.
- I feel a little more comfortable speaking English.
- I can see that daily practice makes a difference.
- I want to continue building my fluency step by step.

Speaking Mission:

Record a 60-second answer:

Why do you want to improve your English speaking?

Reflection:

What changed the most for you in these 7 days?

Completion message:

You completed your 7-Day Fluency Activation. This is only the beginning. Your voice improves when you continue practising the right way.

## 9. Personalisation By Speaking Block

Mouth Flow Block:

Your main focus this week: voice flow and mouth comfort. Pay extra attention to the Voice Flow Drill each day.

Word Availability Block:

Your main focus this week: making useful words ready. Pay extra attention to the Word Combination Drill each day.

Sentence Formation Block:

Your main focus this week: forming complete sentences faster. Pay extra attention to the Sentence Pattern Drill each day.

Grammar Pattern Block:

Your main focus this week: natural grammar through patterns. Do not memorise rules. Repeat patterns aloud.

Expression Block:

Your main focus this week: expressing your real thoughts more naturally. Pay extra attention to the Say It Better Drill each day.

Confidence Block:

Your main focus this week: building speaking comfort. Complete the daily recording even if it is not perfect.

## 10. Progress Tracking Rules

Track:

- current day
- completed days
- streak count
- last completed date
- daily status: locked, unlocked, completed
- completion timestamps
- daily recording URLs
- daily reflections
- paid challenge clicked
- paid challenge joined

Unlock logic:

- Day 1 is unlocked immediately.
- Day 2 unlocks after Day 1 is complete.
- Continue completion-based unlocking until Day 7.
- Missing a day should not punish the user. They continue from the current incomplete day.

## 11. Recording And Reflection Requirements

Each daily practice must include:

- 30-60 second recording
- stop button
- re-record option
- use this recording
- one reflection answer

Completion should require:

- speaking mission recording
- reflection answer

If user did not record:

Please complete your speaking mission before marking today complete. Your voice practice is the most important part.

Re-record microcopy:

You can re-record once, but do not chase perfection. Fluency grows through practice, not perfect recordings.

## 12. Reminder Copy

Reminder structure:

- first name
- day number
- today's theme
- motivational line
- personal access link

### Day 1

Subject: Your Day 1 Fluency Practice Is Ready

Hi [First Name],

Your Day 1 Fluency Activation is ready.

Today's focus: Start Speaking Without Freezing.

You will start slowly, clearly, and without judging yourself.

Continue here: [Personal Link]

Remember: you do not need perfect English to begin. You need to train your voice.

Fluency Magic

### Day 2

Subject: Your Day 2 Fluency Practice Is Ready

Hi [First Name],

Your Day 2 Fluency Activation is ready.

Today's focus: Make Words Come Faster.

You'll practise useful word groups so English starts coming faster when you speak.

Continue here: [Personal Link]

Remember: you do not become fluent by waiting. You become fluent by speaking.

Fluency Magic

### Day 3

Subject: Your Day 3 Sentence Practice Is Ready

Hi [First Name],

Your Day 3 Fluency Activation is ready.

Today's focus: Form Sentences Naturally.

You'll practise patterns that help complete sentences come more easily.

Continue here: [Personal Link]

Small daily speaking practice creates real movement.

Fluency Magic

### Day 4

Subject: Your Day 4 Fluency Practice Is Ready

Hi [First Name],

Your Day 4 practice is ready.

Today's focus: Stop Translating In Your Head.

You'll practise expressing one idea at a time directly in English.

Continue here: [Personal Link]

Speak simply. Speak clearly. Keep going.

Fluency Magic

### Day 5

Subject: Your Day 5 Expression Practice Is Ready

Hi [First Name],

Your Day 5 practice is ready.

Today's focus: Say Simple Things Better.

You'll practise turning basic sentences into more natural spoken English.

Continue here: [Personal Link]

Your real personality deserves stronger English expression.

Fluency Magic

### Day 6

Subject: Your Day 6 Real-Life Speaking Practice Is Ready

Hi [First Name],

Your Day 6 practice is ready.

Today's focus: Speak In A Real Situation.

You'll practise English for work, study, interviews, or real conversations.

Continue here: [Personal Link]

Fluency becomes useful when you practise real situations.

Fluency Magic

### Day 7

Subject: Your Day 7 Fluency Review Is Ready

Hi [First Name],

Your final day is ready.

Today's focus: Review Your Progress.

You'll record again, compare Day 1 and Day 7, and see what daily speaking practice can do.

Continue here: [Personal Link]

This is only the beginning. Your voice improves when you keep training it.

Fluency Magic

## 13. Day 7 Before/After Comparison

Show:

- Day 1 recording
- Day 7 recording
- reflection prompts
- progress checklist

Questions:

- Did you start faster today?
- Did your voice feel easier?
- Did you use better word groups?
- Did your sentences feel more natural?
- Did you feel more confident?

## 14. Paid Challenge Conversion

Do not push too aggressively before Day 7.

Light mention after Day 3:

You have now practised voice flow, word groups, and sentence patterns. These are the foundations of real fluency.

Light mention after Day 5:

You are starting to see how simple English can become more natural with the right practice.

Day 7 paid offer:

Headline:

Ready to Continue Your Fluency Progress?

Copy:

In 7 days, you activated your voice and experienced the Fluency Magic method. But real fluency needs deeper repetition, real-life conversation practice, confidence training, and guided progression.

The 30-Day Fluency Magic Challenge helps you continue with:

- daily structured speaking practice
- deeper word combination mastery
- sentence pattern automation
- expression upgrade drills
- real conversation missions
- before-and-after progress tracking

CTA:

Join the 30-Day Fluency Magic Challenge

Secondary CTA:

Remind Me Later

## 15. UI/UX Requirements

Design should feel:

- premium
- warm
- encouraging
- mobile-first
- app-like
- clean
- modern
- confidence-building
- not childish
- not academic
- not like a school exam

Use:

- progress path
- daily cards
- level badge
- focus badge
- streak indicator
- voice wave animation
- soft gradients
- clear CTA buttons
- simple icons for each drill
- encouraging completion animation

Avoid:

- too much text on one screen
- red error-heavy UI
- school-like marks
- complicated dashboards
- overwhelming analytics
- generic AI chatbot visuals

## 16. Data Fields To Store

User:

- userId
- firstName
- email
- whatsappNumber
- country
- createdAt

Fluency Test:

- overallScore
- fluencyLevel
- mainSpeakingBlock
- subScores
- recommendedPlan

Activation Progress:

- activationStartedAt
- currentDay
- completedDays
- streakCount
- lastCompletedAt
- isCompleted
- day1RecordingUrl
- day7RecordingUrl
- dailyRecordingUrls
- dailyReflections
- dayCompletionStatus
- paidChallengeClicked
- paidChallengeJoined

Daily Practice:

- dayNumber
- status
- recordingUrl
- reflectionAnswer
- completedAt
- timeSpent
- reRecordCount

## 17. Edge Cases

User opens locked day:

Day 3 is not unlocked yet. Complete Day 2 first so your practice builds step by step.

CTA: Go to Day 2

User returns after missing days:

Welcome back. Continue from where you left off. Your next practice is Day [X].

User did not record:

Please complete your speaking mission before marking today complete. Your voice practice is the most important part.

User wants to re-record:

You can re-record once, but do not chase perfection. Fluency grows through practice, not perfect recordings.

User finishes all 7 days:

You completed your 7-Day Fluency Activation.

CTA: View My Progress

CTA: Join 30-Day Challenge

High fluency level:

Your foundation is already strong. Use this 7-day plan to sharpen expression, flow, and confidence.

Low fluency level:

Start simple. Your goal is not perfect English. Your goal is to speak a little more comfortably each day.

## 18. MVP Implementation Notes

Must-have:

- activation dashboard
- seven daily practice pages
- progress saving
- magic link/token access
- daily recording upload
- daily reflection
- mark complete
- Day 7 comparison
- CTA to paid challenge
- email reminders

Can be later:

- full mobile app
- push notifications
- community
- leaderboard
- detailed feedback for every daily recording
- advanced speech analytics
- coach review
- badges
- certificate

## 19. Future App Direction

Future tabs:

1. Today
2. Speaking Gym
3. Word Lab
4. Pattern Gym
5. Say It Better
6. Conversations
7. Progress
8. Profile

Do not build all tabs now. Keep the design and data model flexible for future expansion.
