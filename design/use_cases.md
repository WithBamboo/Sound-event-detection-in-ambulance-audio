# User Story Clustering and Use Cases

## 1. How We Grouped the Stories

We reviewed our 30 user stories and looked for features that different users were asking for, even when they had different reasons for using them.

For example, Tom wants to replay defibrillator charging sounds during a case review, while Sarah wants to replay CPR sounds for training. Their goals are different, but both need a way to select an event and play the corresponding audio.

We grouped stories based on these shared needs. A story can belong to more than one group. We counted each story only once within a theme, and used the number of matching stories to rank the features.

## 2. Themes and Feature Ranking

| Rank | Theme | User Stories | Count |
|---|---|---|---|
| 1 | Audio Playback | 1, 2, 4, 5, 7, 8, 9, 12, 13, 16, 17, 19, 21, 22, 24, 26, 30 | 17 |
| 2 | Event Display & Navigation | 1, 2, 3, 5, 8, 10, 11, 12, 13, 14, 15, 17, 21, 25, 28, 30 | 16 |
| 3 | Detection Review & Validation | 2, 7, 9, 16, 17, 19, 20, 24, 26 | 9 |
| 4 | Event Summaries & Comparison | 6, 10, 14, 18, 20, 21, 24, 27 | 8 |
| 5 | Structured Data Export | 6, 11, 14, 18, 27, 29 | 6 |
| 6 | Filtering & Search | 2, 4, 8, 24 | 4 |
| 7 | Audio Upload & Processing | 20, 23, 25 | 3 |
| 7 | Annotation & Correction | 7, 9, 16 | 3 |

*Counts represent how many of our 30 stories mention each need, not how many real users requested it. Themes overlap, so the total is greater than 30. Features such as audio clip export and confidence indicators are discussed separately below.*

### Theme 1: Audio Playback (17 stories)

This was the most common request. Doctors, paramedics, instructors, and researchers all wanted to listen to specific parts of a recording without going through the entire file.

The main need is to click a detected event and hear the corresponding audio. Some users also want to hear a few seconds before and after an event, especially when checking possible CPR interruptions or incorrect detections.

**Related features:** Play selected audio segments, jump to timestamps, replay surrounding audio.

### Theme 2: Event Display & Navigation (16 stories)

Many users want to understand when events happened and in what order. Some prefer a visual timeline, while others only need a chronological list with timestamps.

The interface should distinguish CPR compression sounds, metronome tones, and defibrillator charging sounds. Users should be able to move from an event in the results to the matching position in the recording.

**Related features:** Event timeline or list, event labels, timestamps, navigation controls.

### Theme 3: Detection Review & Validation (9 stories)

Several stories involve checking whether the model identified sounds correctly. This is especially important because ambulance recordings can contain sirens, speech, vehicle noise, and overlapping equipment sounds.

Users need to compare detected events with the original audio rather than assuming every prediction is correct. Some researchers also want to compare predictions with manually labeled reference data.

**Related features:** Review predictions, inspect uncertain events, compare predictions with reference labels.

### Theme 4: Event Summaries & Comparison (8 stories)

Some users are interested in an overview rather than individual sound events. They want to see what kinds of sounds were detected, how frequently they occurred, or how results differ between recordings.

For example, an EMS coordinator might want event counts for several recordings, while a physician might only need a short summary of one case.

**Related features:** Event counts, recording summaries, cross-recording comparison.

### Theme 5: Structured Data Export (6 stories)

Researchers, analysts, and EMS staff want to reuse the detection results outside the application.

The most useful output would include recording identifiers, event categories, and timestamps in a consistent format. CSV is a reasonable starting point because it can be opened in Excel or processed with Python.

**Related features:** CSV export, structured event records, timestamps.

### Theme 6: Filtering & Search (4 stories)

Users reviewing longer recordings do not always want to see every detected sound. They may only be interested in CPR events, defibrillator charging sounds, or recordings containing possible gaps.

Filtering would make it easier to focus on the relevant results without manually searching through everything.

**Related features:** Filter by event type, search events, filter by gap duration.

### Theme 7: Audio Upload & Processing (3 stories)

A few stories specifically mention uploading recordings and receiving analysis results. Users want a straightforward way to submit an audio file and know whether processing succeeded.

Although this appeared less frequently, it is still essential to the application. Users cannot review new recordings unless the system can accept and process them.

**Related features:** Audio upload, processing status, error messages.

### Theme 8: Annotation & Correction (3 stories)

Researchers and model developers want to flag incorrect predictions or correct event labels and timestamps.

This could help with later model evaluation and dataset improvement. However, editing annotations requires more functionality than simply displaying detection results.

**Related features:** Flag incorrect events, edit labels, adjust timestamps, save corrections.

## 3. Extracted Use Cases

We converted the main themes into use cases describing what a user would actually do with the application.

### UC-01: Upload and Analyze an Audio Recording

**Primary users:** Paramedics, researchers, software testers  
**Related stories:** 20, 23, 25

1. The user selects an audio recording from their computer.
2. The application checks whether the file format is supported.
3. The user starts the analysis.
4. The system processes the audio and produces detected event labels and timestamps.
5. The user sees the results or an error message if processing fails.

**Expected outcome:** The user can submit a supported recording and receive detection results without using the command line.

### UC-02: View and Navigate Detected Events

**Primary users:** Physicians, paramedics, nurses, EMS supervisors  
**Related theme:** Event Display & Navigation

1. The user opens the results for a recording.
2. The application displays detected events in chronological order.
3. Each event includes its type and timestamp.
4. The user selects an event to jump to that position in the recording.

**Expected outcome:** The user can quickly understand the sequence of detected sounds and locate an event of interest.

### UC-03: Play a Selected Audio Segment

**Primary users:** Physicians, EMS instructors, researchers  
**Related theme:** Audio Playback

1. The user selects an event from the results.
2. The application opens the corresponding audio segment.
3. The user plays, pauses, or replays the segment.
4. The user can listen to nearby audio for additional context.

**Expected outcome:** The user can review a relevant sound without listening to the full recording.

### UC-04: Filter Events by Category

**Primary users:** Physicians, paramedics, EMS supervisors  
**Related stories:** 2, 4, 8, 24

1. The user opens a recording's detection results.
2. The user selects an event category, such as CPR or defibrillator charging.
3. The application shows only events matching the selected filter.
4. The user selects a result to inspect its timestamp or audio.

**Expected outcome:** The user can focus on specific types of sounds in a long recording.

### UC-05: Review Possible Detection Errors

**Primary users:** Researchers, quality assurance staff, paramedics  
**Related theme:** Detection Review & Validation

1. The user selects an event or an interval that may contain a detection error.
2. The user listens to the corresponding audio.
3. The user compares what they hear with the predicted event label.
4. Where supported, the user flags a possible error for later review.

**Expected outcome:** The user can check questionable detections instead of relying only on model predictions.

### UC-06: View Event Summaries

**Primary users:** EMS coordinators, physicians, data analysts  
**Related theme:** Event Summaries & Comparison

1. The user opens the results for a recording.
2. The application displays the number of detected events in each category.
3. The user reviews the counts and associated timestamps.
4. If multiple recordings are available, the user can compare their summaries.

**Expected outcome:** The user gets an overview of detected sounds without inspecting each event individually.

### UC-07: Export Detection Results

**Primary users:** Researchers, analysts, software developers  
**Related stories:** 6, 11, 14, 18, 27, 29

1. The user finishes reviewing a recording's detection results.
2. The user selects the export option.
3. The application creates a file containing recording identifiers, event labels, and timestamps.
4. The user downloads the file for documentation or further analysis.

**Expected outcome:** Detection results can be reused in Excel, Python, or other tools without manually copying each event.

### UC-08: Correct Event Annotations

**Primary users:** Research assistants, model developers  
**Related stories:** 7, 9, 16

1. The user selects a predicted event.
2. The user listens to the corresponding audio.
3. The user changes the label or adjusts the timestamp if necessary.
4. The application saves the corrected annotation separately from the original prediction.

**Expected outcome:** Users can prepare reviewed annotations for later analysis and model evaluation.

## 4. What Should We Build First?

The frequency ranking tells us which features appeared most often in our stories, but it does not directly tell us what to implement first.

For example, audio playback ranked first, while upload and processing ranked near the bottom. However, the tool still needs a way to receive and analyze recordings before users can review the results.

Based on the stories, we would start with a relatively small workflow:

1. Upload a recording and run sound detection.
2. Display detected events with labels and timestamps.
3. Allow users to select an event and replay the audio.
4. Add basic filtering by event category.
5. Export the detection results as CSV.

If time allows, we could add event summaries and more detailed review tools. Annotation editing and comparisons across multiple recordings would be useful extensions, but they are not necessary for the first working version.

A few requests also fall outside the main clusters, such as exporting short audio clips, displaying confidence scores, and showing upload errors. We should keep these in mind when deciding the final scope rather than treating every requested feature as equally important.

## 5. Main Takeaway

The strongest pattern across our stories is that users want to find and review relevant sounds quickly without listening to entire ambulance recordings.

This suggests that our project should focus not only on detecting sound events, but also on making those results easy to navigate and verify.

Since detections may be affected by background noise, the application should present results as predictions and allow users to review the original audio. An interval without detected CPR sounds should not automatically be interpreted as proof that CPR stopped. 
