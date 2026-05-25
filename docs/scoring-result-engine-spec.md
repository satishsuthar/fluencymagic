# Fluency Magic Scoring + Result Engine Specification

## Purpose

The Free Fluency Test result should answer three questions:

1. What is my current fluency level?
2. Why do I get stuck while speaking English?
3. What should I practise next?

The result must feel diagnostic, personal, practical, encouraging, and motivating. It should never feel like a school exam or a judgement of intelligence.

## Output Summary

The scoring engine generates:

- Overall Fluency Score
- Six sub-scores
- Fluency Level
- Main Speaking Block
- Short personalised explanation
- Recommended 7-Day Practice Plan
- CTA to start the plan

Routes:

- `/` main landing page
- `/fluency-test` dedicated test flow
- `/fluency-test/result` personalised result page
- `/7-day-plan` recommended practice plan

## Scoring Areas

Each area is scored out of 100.

### 1. Speech Flow

Measures smoothness, pauses, rhythm, hesitation, fillers, and ability to continue speaking.

High score: user continues with fewer pauses and better rhythm.

Low score: user gets stuck, pauses often, or struggles to maintain flow.

### 2. Word Availability

Measures whether useful words come quickly, whether the user uses natural word combinations, and whether they repeat the same basic words too much.

High score: user can access useful words and word groups quickly.

Low score: user may know English, but words are not ready while speaking.

### 3. Sentence Pattern Comfort

Measures complete sentences, common structures, sentence expansion, grammar confusion, and broken or unnatural patterns.

High score: sentences form naturally and complete thoughts are expressed.

Low score: user knows words but struggles to build clear sentences quickly.

### 4. Expression Clarity

Measures whether ideas are clear, meaningful, detailed, organised, and easy to understand.

High score: user communicates ideas clearly.

Low score: user may speak words, but the message is unclear, incomplete, or underdeveloped.

### 5. Naturalness

Measures natural conversational quality, less translation-style English, natural word order, and common phrases.

High score: user sounds more natural and conversational.

Low score: user may be translating mentally or using stiff structures.

### 6. Speaking Confidence

Measures voice steadiness, willingness to continue, energy, self-assurance, and nervousness.

High score: user sounds steady and confident.

Low score: user may know English, but nervousness blocks expression.

## Overall Score Logic

MVP formula can use a simple average:

```text
Overall Fluency Score = average of all six sub-scores
```

Current implementation uses a speaking-first weighted formula:

```text
Speech Flow: 20%
Word Availability: 20%
Sentence Pattern Comfort: 20%
Expression Clarity: 15%
Naturalness: 15%
Speaking Confidence: 10%
```

This fits Fluency Magic because the brand is focused on real speaking fluency, not academic English.

## Fluency Levels

### Level 1: Silent Understander

Score range: 0-25

Headline: Your voice is ready to start moving.

Description: You may understand some English, but speaking feels uncomfortable or difficult. You may avoid speaking, stop after a few words, or feel unsure about how to begin.

What this means: Your English may be sitting in your mind, but it is not yet ready on your tongue.

Next focus:

- Short speaking drills
- Mouth flow practice
- Simple sentence patterns
- Daily 30-second speaking habit
- Confidence-building repetition

Encouraging line: You do not need to speak perfectly. You need to start training your voice step by step.

CTA sentence: Start your free 7-day plan and begin training your voice step by step.

### Level 2: Hesitant Speaker

Score range: 26-45

Headline: You have English inside you. Now it needs to flow.

Description: You can speak some English, but you may pause often, translate in your mind, search for words, or worry about grammar while speaking.

What this means: You are not starting from zero. You already understand English. But your speaking system needs daily practice so words come faster and sentences form more naturally.

Next focus:

- Speech flow drills
- Word combination practice
- Sentence pattern training
- Daily speaking missions
- Reducing translation habit

Encouraging line: You are not starting from zero. You already have English inside you. Now we need to make it flow.

CTA sentence: Start your free 7-day plan and begin training your speaking flow today.

### Level 3: Functional Speaker

Score range: 46-65

Headline: Your foundation is there. Now your expression needs more range.

Description: You can communicate basic ideas in English, but your speech may feel slow, simple, repetitive, or not fully natural.

What this means: You can speak, but you may not express your complete personality, ideas, confidence, or intelligence in English yet.

Next focus:

- Natural word groups
- Sentence expansion
- Expression upgrade drills
- Real-life conversation practice
- Storytelling practice

Encouraging line: Your foundation is already there. Now Fluency Magic will help you sound more natural, clear, and confident.

CTA sentence: Start your free 7-day plan and strengthen your natural expression.

### Level 4: Natural Speaker

Score range: 66-82

Headline: You are close to strong fluency.

Description: You can speak clearly in many situations, but you may still need more polish, smoother expression, professional fluency, and stronger confidence in important moments.

What this means: You are already communicating well, but you can become sharper, more expressive, and more powerful in interviews, meetings, presentations, and deeper conversations.

Next focus:

- Advanced expression
- Professional speaking practice
- Storytelling
- Interview and meeting fluency
- Confident communication presence

Encouraging line: You are close to strong fluency. Now the focus is polish, presence, and powerful expression.

CTA sentence: Start your free 7-day plan and polish your speaking presence.

### Level 5: Confident Communicator

Score range: 83-100

Headline: Your voice is already strong.

Description: You speak with clarity, flow, and confidence. You can express your ideas naturally and handle many real-life English situations well.

What this means: Your next level is not basic fluency. Your next level is influence, storytelling, professional presence, emotional expression, and powerful communication.

Next focus:

- Leadership communication
- Advanced storytelling
- Persuasive speaking
- Presentation fluency
- High-level professional expression

Encouraging line: Your voice is already strong. Now we help you make it more powerful, precise, and memorable.

CTA sentence: Start your free 7-day plan and sharpen your advanced expression.

## Speaking Block Diagnosis Logic

Choose one main speaking block.

Primary rule: choose the block connected to the lowest sub-score.

Special rule: if Naturalness is low and Sentence Pattern Comfort is also low, choose Grammar Pattern Block.

Tie priority:

1. Speech Flow
2. Word Availability
3. Sentence Pattern Comfort
4. Speaking Confidence
5. Expression Clarity
6. Naturalness

Mapping:

- Speech Flow lowest -> Mouth Flow Block
- Word Availability lowest -> Word Availability Block
- Sentence Pattern Comfort lowest -> Sentence Formation Block
- Naturalness low and Sentence Pattern Comfort low -> Grammar Pattern Block
- Expression Clarity lowest -> Expression Block
- Speaking Confidence lowest -> Confidence Block

## Speaking Block Templates

### Mouth Flow Block

Simple explanation: You may know what you want to say, but your mouth, tongue, breath, and voice are not yet comfortable producing English smoothly.

Why this happens: English has not been practised enough as a physical speaking skill. You may understand English mentally, but your speech organs need repeated practice to make English feel easy.

What to practise:

- Short phrase repetition
- Mouth movement drills
- Slow-clear-fast speaking practice
- Sentence expansion
- Daily voice practice

Recommended plan focus: 7-Day Voice Flow Activation.

CTA sentence: Start your free 7-day plan and train your voice flow.

### Word Availability Block

Simple explanation: You may know many words, but useful words and word groups do not come quickly while speaking.

Why this happens: Most learners memorise isolated words, but fluent speakers use natural word combinations. If word groups are not ready, you pause and search while speaking.

What to practise:

- Word combination drills
- Core word mastery
- Phrase group practice
- Verb-noun combinations
- Speaking with common expressions

Recommended plan focus: 7-Day Word Combination Activation.

CTA sentence: Start your free 7-day plan and make useful word groups ready for speaking.

### Sentence Formation Block

Simple explanation: You may know words, but full sentences do not form naturally and quickly.

Why this happens: Your mind may be collecting words one by one instead of using ready sentence patterns.

What to practise:

- Sentence pattern drills
- Sentence expansion practice
- Common speaking structures
- Repeated pattern-based practice

Recommended plan focus: 7-Day Sentence Pattern Activation.

CTA sentence: Start your free 7-day plan and train complete spoken sentences.

### Grammar Pattern Block

Simple explanation: You may think too much about grammar while speaking, and that breaks your flow.

Why this happens: Grammar has been learned as rules, not as natural speaking patterns. When you speak, your mind checks correctness instead of expressing ideas.

What to practise:

- Pattern-based grammar practice
- Natural sentence repetition
- Common tense structures through speaking
- Grammar without rule memorisation

Recommended plan focus: 7-Day Natural Grammar Pattern Activation.

CTA sentence: Start your free 7-day plan and practise grammar as speaking patterns.

### Expression Block

Simple explanation: You can say basic things, but your real thoughts, feelings, and personality do not fully come out in English.

Why this happens: You may be using very simple sentences or direct translations. Your English needs more natural expression, detail, and emotional range.

What to practise:

- Say It Better drills
- Opinion speaking
- Storytelling practice
- Emotion and feeling expression
- Real-life speaking missions

Recommended plan focus: 7-Day Expression Upgrade Activation.

CTA sentence: Start your free 7-day plan and upgrade your expression.

### Confidence Block

Simple explanation: Your English may be better than you think, but nervousness, fear, or self-doubt blocks your speaking.

Why this happens: You may have had negative experiences, fear of mistakes, or lack of safe speaking practice. The pressure of speaking makes your mind go blank.

What to practise:

- Safe daily recording practice
- Low-pressure speaking tasks
- Repetition
- Confidence-building feedback
- Gradual real-life speaking challenges

Recommended plan focus: 7-Day Speaking Confidence Activation.

CTA sentence: Start your free 7-day plan and build speaking comfort.

## Result Page Structure

1. Supportive Header

Headline: Your Fluency Snapshot Is Ready

Subheadline: This is not a judgement of your intelligence or potential. It is a simple diagnosis of where your spoken English gets stuck and what to practise next.

2. Overall Score Card

Show overall score, fluency level, and short explanation.

3. Score Breakdown

Show six score cards:

- Speech Flow
- Word Availability
- Sentence Pattern Comfort
- Expression Clarity
- Naturalness
- Speaking Confidence

Each card includes score, short label, and one-line explanation.

4. Main Speaking Block Card

Headline: Your Main Speaking Block

Show block name, meaning, why it happens, and what helps.

5. What This Means

Explain that the result does not mean the user's English is bad. It means their speaking system needs the right kind of practice.

6. Recommended Practice Path

Headline: Your Recommended Next Step

CTA: Start My Free 7-Day Plan

7. Motivational Close

Headline: You Do Not Become Fluent by Waiting. You Become Fluent by Speaking.

Copy: You do not need perfect English before you begin. You need the right speaking practice, repeated daily. Fluency Magic will help you train your voice, words, sentence patterns, and confidence step by step.

## 7-Day Plan Recommendation Logic

Mouth Flow Block -> 7-Day Voice Flow Activation.

Focus: Train mouth, breath, rhythm, and speaking flow.

Word Availability Block -> 7-Day Word Combination Activation.

Focus: Make useful words and natural word groups ready for speaking.

Sentence Formation Block -> 7-Day Sentence Pattern Activation.

Focus: Make common sentence structures automatic.

Grammar Pattern Block -> 7-Day Natural Grammar Pattern Activation.

Focus: Practise grammar as speaking patterns, not rules.

Expression Block -> 7-Day Expression Upgrade Activation.

Focus: Say basic ideas in clearer, more natural, and more confident ways.

Confidence Block -> 7-Day Speaking Confidence Activation.

Focus: Build comfort through safe, simple, daily speaking practice.

Each recommendation includes plan name, why it is recommended, what the user will practise, what improvement they can expect, and CTA.

## Edge Cases

Very short recording: We need a little more speaking to understand your fluency clearly. Please record at least 30 seconds.

Silent recording: We could not detect enough speech. Try again in a quiet place and speak naturally.

Poor audio quality: Your voice was difficult to hear clearly. Please try again with less background noise.

One-word answers: Try to speak in full sentences so we can give you a more useful fluency report.

Analysis/transcription failure: This is a preliminary fluency snapshot based on your answers. Your detailed voice-based report could not be generated right now.

High score: You already have a strong foundation. Your next level is advanced expression, professional fluency, storytelling, and confident presence.

Very low score: This is a starting point, not a limitation. Your first goal is simple speaking comfort, not perfection.

## UI/UX Requirements

The result page should feel personal, premium, encouraging, clear, non-academic, gentle, and mature.

Required elements:

- Score circle or progress bar
- Level badge
- Six sub-score cards
- Main speaking block card
- Recommended plan card
- CTA button
- Soft motivational copy
- Clean mobile-first design
- No red failure styling

CTA appears at least three times:

- Near top after score
- After speaking block explanation
- At bottom after motivational close

Primary CTA: Start My Free 7-Day Plan

Secondary CTA: Retake Fluency Test

## Data Output Structure

```json
{
  "overallScore": 42,
  "fluencyLevel": {
    "levelNumber": 2,
    "levelName": "Hesitant Speaker",
    "scoreRange": "26-45",
    "headline": "You Have English Inside You. Now It Needs to Flow.",
    "description": "...",
    "nextFocus": ["Speech Flow", "Word Combinations", "Sentence Patterns"],
    "encouragingLine": "..."
  },
  "subScores": {
    "speechFlow": 38,
    "wordAvailability": 41,
    "sentencePatternComfort": 45,
    "expressionClarity": 48,
    "naturalness": 39,
    "speakingConfidence": 36
  },
  "mainSpeakingBlock": {
    "blockName": "Word Availability Block",
    "meaning": "...",
    "whyItHappens": "...",
    "recommendedPractice": ["Word Combination Drills", "Core Word Mastery", "Phrase Group Practice"]
  },
  "recommendedPlan": {
    "planName": "7-Day Word Combination Activation",
    "focus": "Make useful words and natural word groups ready for speaking.",
    "cta": "Start My Free 7-Day Plan"
  }
}
```

## Developer Notes

Current MVP uses a local browser scoring heuristic based on self-assessment answers, confidence rating, practice frequency, whether recording was completed, and browser-generated transcripts when available.

Browser-local transcription:

- Uses `MediaRecorder` for audio capture.
- First attempts live browser speech recognition during recording when supported.
- Uses Transformers.js with a small Whisper model as a local decoded-audio fallback when supported.
- Shows the transcript on the recording screen.
- Uses transcript signals such as word count, speaking rate, filler words, sentence markers, target word usage, and sentence-pattern hits.
- Does not upload audio to a Fluency Magic server in the static prototype.

Production scoring should add:

- Optional secure upload for audio recordings if the user consents to server-side analysis.
- More robust transcription for all speaking tasks if browser-local transcription is not enough.
- Transcript-based scoring for pauses, fillers, word search, sentence completeness, word-combination quality, clarity, naturalness, and ability to continue.
- Optional voice-signal scoring only when technically reliable and consented.
- Fallback preliminary result when transcription fails.
- Versioned scoring model so result interpretation can improve without breaking historical reports.
- Analytics events for test start, question answered, recording completed, lead submitted, result viewed, and plan CTA clicked.

Avoid language that sounds like failure. The product should say "block," "focus," "next step," and "practice path," not "wrong," "bad," or "failed."
