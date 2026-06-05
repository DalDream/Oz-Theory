# MVP PRD: Division 1 OS

## PSYCHO-PASS Narrative Action Interface Prototype

## 1. Product Summary

**Division 1 OS** is a personal narrative action interface inspired by the PSYCHO-PASS universe.

The user plays the role of **Kogami Shinya**, and the AI assistant plays the role of **Inspector Akane Tsunemori**.

The app transforms the user’s real daily life into a Public Safety Bureau investigation flow:

* Morning status → operation briefing
* Daily tasks → mission cards
* Real-life friction → tactical reframing
* Natural reports → Akane responses
* End of day → final case report

The goal is to make daily planning, action, and reflection more immersive and easier to sustain.

---

## 2. Core User Flow

1. User opens the app in the morning.
2. User enters only 4 fields:

   * Wake time
   * Sleep hours
   * Current condition
   * Today’s rough tasks
3. The app generates:

   * Psycho-Pass / Hue status
   * Akane’s morning briefing
   * Mission cards for today
4. User reports throughout the day in natural language.
5. Akane responds in PSYCHO-PASS worldbuilding language.
6. At the end of the day, user taps **Generate Final Case Report**.
7. The app generates a fixed-format investigation report.
8. User saves or copies the report.

---

## 3. MVP Screens

## Screen 1. Morning Briefing

### Purpose

Let the user start the day with minimum input and receive an immersive mission briefing from Akane.

### Input Fields

Only include these fields:

1. **Wake Time**

   * Example: `10:20`

2. **Sleep Hours**

   * Example: `7`

3. **Current Condition**

   * Options:

     * Very Good
     * Good
     * Normal
     * Bad
     * Very Bad

4. **Today’s Rough Tasks**

   * Long text field
   * Example:
     `Go to the Busan base, complete 2 Study Jam badges, review Stitch, and prepare the Narrative OS prototype.`

### Primary Button

`Connect to Division 1`

### Output After Submission

Generate and display:

1. **Hue / Psycho-Pass Status**
2. **Akane’s Morning Briefing**
3. **Today’s Mission Cards**

### Example Output Structure

```text
⚖️ [Public Safety Bureau Division 1: Morning Briefing]

Kogami-san, morning status confirmed.

Current Status:
- Sleep: 7 hours
- Condition: Normal
- Hue Status: Slightly Clouded
- Psycho-Pass Stability: 72/100

Today’s Operation:
1. Secure 2 Study Jam badges
2. Review Stitch and AI Studio
3. Prepare the Narrative OS prototype

Akane’s Directive:
Focus on the first target. Do not expand the scope before the first mission is secured.
```

---

## Screen 2. Secure Channel

### Purpose

Main conversation screen between Kogami and Akane.

### UI Requirements

* Dark cyber investigation interface
* Header:
  `DIVISION 1 SECURE CHANNEL`
* Show today’s date
* Show current Hue / Stability status
* Chat bubbles:

  * User: Kogami Shinya
  * AI: Akane Tsunemori
* Profile avatars or initials:

  * KOGAMI
  * AKANE
* Long text input field
* Send button
* Fixed bottom button:
  `Generate Final Case Report`

### No Quick Report Buttons

The user should report naturally by typing.

Examples:

```text
Akane Inspector, I have arrived at the Busan base.
```

```text
Akane Inspector, I secured the first badge.
```

```text
Akane Inspector, I need to make an administrative phone call, but I don’t have the mental energy for it.
```

The AI should infer the report type from natural language.

---

## Screen 3. Mission Cards

### Purpose

Show today’s rough tasks as immersive operation cards.

Mission cards are generated from the morning task input.

### Mission Card Format

```text
CASE 01
Study Jam Badge Lock-on

Objective:
Secure 2 Study Jam badges.

Status:
LOCK-ON

Risk:
Distraction, scope expansion, fatigue.

Akane’s Directive:
Aim at the first target precisely before moving to the next.
```

### Mission Status Options

* `LOCK-ON`
* `IN PROGRESS`
* `SECURED`
* `DEFERRED`

### Requirements

* User can manually change mission status.
* Mission cards should feel like investigation files, not productivity checklists.

---

## Screen 4. Final Case Report

### Purpose

Generate a fixed-format final report at the end of the day.

### Button

`Generate Final Case Report`

### Data Used

Use:

* Morning input
* Mission cards
* Mission status
* Full conversation log
* User’s final report request

### Report Actions

* Save Report
* Copy Report
* Regenerate Report

### Fixed Report Format

The final report must always follow this structure.

```text
📂 [Case Report] YYYY-MM-DD Enforcer Kogami Shinya Investigation Record

1. Strategic Architecture: [Grade]
Analysis:
- Evaluate today’s planning, startup thinking, idea development, strategic pivot, and technical application based on real actions.

Assessment:
"Interpret today’s strategic meaning using PSYCHO-PASS worldbuilding language."

2. Mission Execution: [Grade]
Analysis:
- Evaluate completed learning, development, writing, meetings, administrative work, movement, or part-time work.

Assessment:
"Reframe completed real-world actions as investigation progress or secured evidence."

3. Mental Resilience: [Grade]
Analysis:
- Evaluate how the user handled fatigue, stress, distraction, self-doubt, family noise, or emotional friction.

Assessment:
"Focus on recovery, return-to-action, and noise control rather than failure."

4. Self-Maintenance: [Grade]
Analysis:
- Evaluate sleep, food, movement, rest, physical condition, and recovery behavior.

Assessment:
"Use Psycho-Pass, Hue, and Crime Coefficient only as metaphors for fatigue and overload. Do not treat them as real mental health measurements."

📝 [Inspector Akane’s Personal Comment]
"Write a short but meaningful comment about the user’s identity shift, strongest moment of the day, and one sentence to carry into tomorrow."

🎯 [Tomorrow’s Tactical Directives]
1.
2.
3.
```

### Grade System

Use the following grade system:

```text
S+  : Critical progress in long-term project, identity, or business direction
S   : Core missions completed with strong immersion
A++ : Fatigue or interference existed, but the user recovered and returned to action
A+  : Stable execution of major tasks
A   : Basic mission execution with no major collapse
B   : Unstable execution, but user returned and recorded the day
C   : Collapse or stagnation occurred, but useful observation data was secured
```

---

## Screen 5. Archive

### Purpose

Store and view saved final case reports.

### Archive Card Format

Each saved report appears as a card.

```text
2026-06-05
CASE FILE CLOSED

Representative Grade:
Strategic Architecture [S]

Main Mission:
Study Jam Badge Lock-on

Akane Comment Preview:
"Kogami-san, today you were not merely learning tools. You were preparing the architecture of a larger system."
```

### Functions

* Open report
* Copy report
* Delete report
* Search by date

---

## 4. AI Role Definition

Use the following system instruction for Gemini.

```text
You are Inspector Akane Tsunemori from the PSYCHO-PASS universe.
The user is Enforcer Kogami Shinya.

Your role is to transform the user’s real daily life into the language of Public Safety Bureau Division 1 operations.

You help the user plan, act, recover, and reflect by reframing real-world actions as investigations, missions, evidence collection, tactical adjustments, and case reports.

Core rules:
- Call the user “Kogami-san.”
- Speak as Akane: calm, observant, warm, but firm.
- Maintain the PSYCHO-PASS universe.
- Reframe real-life actions into investigation language.
- Help the user take action in reality.
- Do not encourage avoidance of real life.
- Do not behave like a therapist.
- Do not diagnose mental health.
- Treat Psycho-Pass, Hue, Crime Coefficient, Dominator, and Sibyl as metaphors only.
- Avoid excessive praise.
- Avoid overly long responses unless generating the final case report.
- For normal replies, keep the response concise and actionable.
- Give no more than 3 tactical directives at once.

Worldbuilding mapping:
- Office or workspace = Busan Base
- Studying or training = investigation training / evidence acquisition
- Study Jam badge = evidence target
- PeachRun = long-term investigation project
- Business evaluation or judges = Sibyl System judgment protocol
- Administrative work = Sibyl administrative gate
- Part-time work = ammunition acquisition operation
- Fatigue = Hue clouding / Crime Coefficient rise risk
- Rest = Hue stabilization protocol
- Failure = collapse data / tactical adjustment signal
- Distraction = investigation noise
- Difficult task = resistance node

When the user reports friction, use this 3-step response:
1. Confirm the friction.
2. Reframe the task as a meaningful operation inside the PSYCHO-PASS universe.
3. Give one immediate first action.

When generating the final case report, always follow the fixed report format exactly.
```

---

## 5. Friction Reframing Behavior

When the user says they are avoiding or delaying something, Akane should respond like this.

### Example User Input

```text
Akane Inspector, I need to make an administrative phone call, but I really don’t want to do it.
```

### Example AI Output

```text
Kogami-san, avoidance response confirmed.

This call is not a simple administrative task.
It is a Sibyl administrative gate blocking the next phase of the investigation.

If this node remains unresolved, it will continue to create background noise in your operation.

Tactical directive:
1. Open the contact page.
2. Prepare only the first sentence.
3. Make the call within 3 minutes.

Report back immediately after completion. I will record it as a cleared resistance node.
```

---

## 6. Hue / Psycho-Pass Status Logic

Use a simple rule-based status for MVP.

### Condition Mapping

```text
Very Good → Hue Status: Clear / Stability: 90
Good → Hue Status: Stable / Stability: 80
Normal → Hue Status: Slightly Clouded / Stability: 70
Bad → Hue Status: Clouded / Stability: 55
Very Bad → Hue Status: Operation Caution / Stability: 40
```

### Sleep Adjustment

```text
Sleep >= 7 hours: +5 Stability
Sleep 5–6.9 hours: +0 Stability
Sleep < 5 hours: -10 Stability
```

### Important Rule

The stability score is not a medical or mental health measurement.
It is only a narrative metaphor for fatigue, overload, and operational readiness.

---

## 7. Data Model

Use a simple local or Firebase-compatible structure.

### DailySession

```json
{
  "id": "2026-06-05",
  "date": "2026-06-05",
  "wakeTime": "10:20",
  "sleepHours": 7,
  "condition": "Normal",
  "hueStatus": "Slightly Clouded",
  "stabilityScore": 75,
  "roughTasks": "Go to the Busan base, complete 2 Study Jam badges, review Stitch, and prepare the Narrative OS prototype.",
  "createdAt": "timestamp",
  "updatedAt": "timestamp"
}
```

### MissionCard

```json
{
  "id": "mission_001",
  "date": "2026-06-05",
  "caseNumber": "CASE 01",
  "title": "Study Jam Badge Lock-on",
  "objective": "Secure 2 Study Jam badges.",
  "status": "LOCK-ON",
  "risk": "Distraction, scope expansion, fatigue.",
  "akaneDirective": "Aim at the first target precisely before moving to the next.",
  "createdAt": "timestamp",
  "updatedAt": "timestamp"
}
```

### Message

```json
{
  "id": "msg_001",
  "date": "2026-06-05",
  "role": "user",
  "persona": "Kogami Shinya",
  "content": "Akane Inspector, I have arrived at the Busan base.",
  "createdAt": "timestamp"
}
```

### FinalReport

```json
{
  "id": "report_2026_06_05",
  "date": "2026-06-05",
  "content": "Full final case report text",
  "representativeGrade": "S",
  "akaneComment": "Kogami-san, today you were not merely learning tools...",
  "nextDirectives": [
    "Secure the first target before expanding scope.",
    "Keep tomorrow’s operation narrow.",
    "Start recovery protocol before midnight."
  ],
  "createdAt": "timestamp"
}
```

---

## 8. Stitch Build Prompt

Use this in Stitch to generate the prototype UI.

```text
Build a mobile-first dark cyber investigation web app called “Division 1 OS”.

The app is inspired by the PSYCHO-PASS Public Safety Bureau Division 1 interface.

The user is Kogami Shinya.
The AI assistant is Inspector Akane Tsunemori.

Core screens:
1. Morning Briefing
2. Secure Channel
3. Mission Cards
4. Final Case Report
5. Archive

Design:
- Dark navy / black background
- Cyan and blue accent colors
- Futuristic official investigation system
- Minimal, immersive, text-focused
- Korean UI labels
- Not cute, not gamified, not a normal productivity app
- Use cards, terminal-like panels, and secure-channel styling

Morning Briefing screen:
- Header: PUBLIC SAFETY BUREAU / DIVISION 1
- Input fields:
  - 기상시간
  - 수면시간
  - 컨디션
  - 오늘 대략 할 일
- Button: 공안국 1계 접속
- After submission, show:
  - 색상 안정도
  - Psycho-Pass Stability score
  - 아카네의 아침 브리핑
  - 오늘의 작전 카드

Secure Channel screen:
- Header: DIVISION 1 SECURE CHANNEL
- Show today’s date, Hue Status, Stability Score
- Chat UI with two personas:
  - 코가미 신야
  - 츠네모리 아카네
- Long text input
- Send button
- Fixed bottom button: 최종 수사보고서 생성
- No quick report buttons

Mission Cards:
- Display mission cards generated from today’s rough tasks
- Each card includes:
  - CASE number
  - title
  - objective
  - status
  - risk
  - Akane directive
- Status options:
  - LOCK-ON
  - IN PROGRESS
  - SECURED
  - DEFERRED

Final Case Report screen:
- Button: 최종 수사보고서 생성
- Show report in fixed evaluation format
- Buttons:
  - 저장
  - 복사
  - 다시 생성

Archive screen:
- Show saved reports by date
- Each archive card includes:
  - date
  - representative grade
  - main mission
  - Akane comment preview
```

---

## 9. MVP Success Criteria

The MVP is successful if:

1. The user can start the day with only 4 inputs.
2. The app generates an immersive Akane morning briefing.
3. The app creates mission cards from rough tasks.
4. The user can naturally report throughout the day without using quick buttons.
5. Akane can reframe friction into immediate action.
6. The final case report follows the fixed evaluation format.
7. The user prefers this app over Notion for daily narrative reporting.

```
```
