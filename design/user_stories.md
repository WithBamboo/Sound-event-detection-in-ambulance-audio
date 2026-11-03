Who is the user. What do they want to do with the tool. What needs and desires do they want for the tool. What is their skill level.

Take 20 mins to write at least 30 user stories in this format in the markdown file you just created. After a couple, flag an instructional team member for input before you write all 30. 

The doctor is user. They want to use this tool do understand what happens 

### User 1: Tom
Tom is a 50-year-old emergency physician receiving a patient after ambulance transport. He wants to locate and replay sections of the recording containing defibrillator charging sounds so that he can review when these sounds occurred during resuscitation. He needs clickable timestamps and short audio clips rather than having to listen to the entire recording. He is comfortable using graphical clinical software but has no command-line experience.

### User 2: Mary
Mary is a 40-year-old cardiologist reviewing a 20-minute ambulance recording after a resuscitation. She wants to find possible pauses between detected CPR compression sounds without listening to the entire recording. She needs to filter the timeline to show CPR events, see the start and end timestamps of each detected interval, and click a possible gap to hear the audio immediately before and after it. She wants to check these clips herself because background noise may cause the tool to miss compression sounds. Mary uses graphical clinical software daily but has no programming or command-line experience.

### User 3: James
James is a 35-year-old paramedic reviewing an ambulance recording after a difficult emergency call. He wants to see a timeline of detected CPR compression sounds, metronome tones, and defibrillator charging sounds to understand the sequence of events during transport. He needs different event types to be clearly labeled and displayed in chronological order. He regularly uses electronic patient care reporting systems but has no programming experience.

### User 4: Sarah
Sarah is a 42-year-old EMS training instructor preparing a CPR training session for new paramedics. She wants to find examples of consistent and interrupted CPR compressions from recorded ambulance scenarios. She needs to search for CPR events, select a short section of audio, and replay it during training. She is comfortable using presentation software and basic audio players but does not know how to use Python or command-line tools.

### User 5: David
David is a 29-year-old emergency medical technician reviewing a recording after completing a patient transport. He wants to check whether metronome sounds were detected throughout a CPR session. He needs a timeline showing where metronome tones were detected and where there may have been interruptions, with the option to listen to those sections. He is familiar with mobile applications and electronic medical records but has limited experience with audio analysis software.

### User 6: Emily
Emily is a 38-year-old EMS quality improvement coordinator reviewing multiple emergency transport recordings. She wants to compare the number and timing of detected CPR and defibrillator-related events across recordings to identify cases that may need further review. She needs a summary of detected events for each recording and the ability to download the results as a CSV file. She regularly uses Excel and reporting dashboards but has no programming background.

### User 7: Michael
Michael is a 26-year-old medical research assistant studying sound events in ambulance recordings. He wants to compare automatically detected events with manually labeled audio segments to understand how accurately the tool identifies different sounds. He needs to view predicted timestamps, listen to corresponding audio clips, and record whether each prediction is correct. He has basic Python and data analysis experience.

### User 8: Linda
Linda is a 45-year-old ambulance operations supervisor reviewing a recording after an emergency response. She wants to quickly locate defibrillator charging sounds without listening to the entire recording. She needs a list of detected events with timestamps and the ability to jump directly to each audio segment. She uses scheduling and reporting software daily but has no programming background.

### User 9: Alex
Alex is a 24-year-old computer science student helping improve an ambulance sound detection model. He wants to find audio segments where the model may have confused background ambulance noise with CPR or metronome sounds. He needs to review predicted event labels, listen to the audio, and mark incorrect detections for further analysis. He is comfortable using Python, GitHub, and basic machine learning tools.

### User 10: Rachel
Rachel is a 33-year-old emergency department nurse receiving a patient from an ambulance team. She wants to review a concise timeline of detected resuscitation-related sounds to better understand what happened during transport. She needs to see event types and approximate timestamps without navigating through the full recording. She is experienced with electronic health record systems but has no programming experience.

### User 11: Kevin
Kevin is a 31-year-old paramedic completing documentation after an emergency transport. He wants to use detected sound events to help reconstruct the sequence of resuscitation activities. He needs a chronological list of events with timestamps that he can reference while writing his report. He is familiar with electronic documentation systems but has no programming experience.

### User 12: Olivia
Olivia is a 36-year-old emergency physician reviewing an ambulance recording with several overlapping sounds. She wants to listen to specific segments where CPR compressions and defibrillator charging sounds may have occurred close together. She needs the tool to display multiple detected event types on the same timeline and allow her to replay those segments. She regularly uses clinical software but has no audio processing experience.

### User 13: Daniel
Daniel is a 27-year-old paramedic instructor reviewing a training recording with students. He wants to compare periods of detected CPR compression sounds with metronome tones to discuss whether compressions followed the training rhythm. He needs both event types displayed together and the ability to replay selected intervals. He is comfortable with graphical training software but has no programming experience.

### User 14: Sophia
Sophia is a 30-year-old healthcare data analyst evaluating ambulance sound detection results. She wants to identify how many events of each type were detected in a recording. She needs a summary showing counts for CPR compressions, metronome tones, and defibrillator charging sounds, with an option to export the results. She is proficient in Excel and SQL and has basic Python experience.

### User 15: Brian
Brian is a 43-year-old EMS supervisor reviewing a long emergency transport recording. He wants to skip sections without relevant detected events and focus on periods containing resuscitation-related sounds. He needs an event timeline with clickable timestamps that let him jump directly to important sections. He regularly uses office and reporting software but has no programming experience.

### User 16: Hannah
Hannah is a 25-year-old research assistant preparing an annotated audio dataset. She wants to manually correct event labels when the detection model identifies the wrong sound. She needs to edit event categories and timestamps while listening to the corresponding recording. She has experience with Python and basic audio annotation tools.

### User 17: Robert
Robert is a 48-year-old EMS quality assurance manager reviewing possible interruptions during CPR. He wants to identify intervals where compression sounds were not detected for an extended period. He needs the tool to highlight possible gaps and allow him to listen to the surrounding audio before deciding whether an interruption occurred. He is familiar with clinical reporting applications but has no programming experience.

### User 18: Jessica
Jessica is a 34-year-old emergency medicine researcher studying patterns in resuscitation recordings. She wants to compare the timing of detected CPR sounds and defibrillator charging events to understand how these events were distributed during transport. She needs timestamped event data that can be exported for further analysis. She regularly uses statistical software and has intermediate Python experience.

### User 19: Andrew
Andrew is a 39-year-old paramedic reviewing a recording with loud ambulance sirens and conversations. He wants to know which detected events may be less reliable because of background noise. He needs the tool to display confidence scores or uncertainty indicators for detected sounds so he can decide which sections require manual review. He uses clinical software regularly but has no machine learning background.

### User 20: Natalie
Natalie is a 28-year-old graduate student testing a sound detection model on ambulance recordings. She wants to compare predictions across recordings with different levels of background noise. She needs a way to upload recordings, review detected event timestamps, and compare the results with reference labels. She is comfortable with Python, data visualization, and basic machine learning.

### User 21: Peter
Peter is a 52-year-old emergency physician with limited time between patients. He wants to understand the main detected events in an ambulance recording without listening to the full audio. He needs a simple summary showing event types, counts, and approximate timestamps. He is comfortable with electronic medical record systems but has no programming experience.

### User 22: Grace
Grace is a 32-year-old EMS training coordinator creating educational materials from recorded emergency scenarios. She wants to save short audio clips containing CPR compressions, metronome tones, or defibrillator charging sounds for training discussions. She needs to select a time range and export the corresponding audio segment. She regularly uses presentation and video editing software but has no programming background.

### User 23: Ethan
Ethan is a 23-year-old computer science student testing the ambulance audio detection application. He wants to know whether the system processes an uploaded recording successfully and displays the detected events. He needs clear upload status messages, error notifications, and confirmation when analysis is complete. He is comfortable with Python and basic software testing.

### User 24: Victoria
Victoria is a 41-year-old hospital quality improvement specialist reviewing several ambulance cases. She wants to identify recordings with unusually long intervals between detected CPR compression sounds. She needs to filter recordings based on possible interruption duration and open the relevant audio segments for review. She is experienced with Excel and clinical reporting dashboards but has no programming experience.

### User 25: Chris
Chris is a 37-year-old ambulance paramedic using a shared workstation after an emergency call. He wants to upload an ambulance recording and review detected sound events without installing additional software. He needs a browser-based interface with simple upload controls and clearly labeled results. He regularly uses web applications but has no command-line experience.

### User 26: Mia
Mia is a 29-year-old biomedical engineering researcher investigating the performance of sound detection models. She wants to examine cases where CPR compression sounds overlap with speech or vehicle noise. She needs to inspect the detected timestamps, review the original audio, and compare predicted labels with manually verified events. She has experience with Python, signal processing, and machine learning.

### User 27: George
George is a 46-year-old EMS operations manager preparing a report on emergency transport recordings. He wants to summarize how frequently different resuscitation-related sounds were detected across reviewed cases. He needs a table of event counts by recording and the ability to export the results to CSV. He is familiar with Excel and business reporting software but has no programming experience.

### User 28: Lily
Lily is a 27-year-old emergency department nurse reviewing an ambulance recording during a patient handoff. She wants to quickly distinguish CPR compression events from metronome tones and defibrillator charging sounds. She needs clearly labeled event categories, different visual indicators, and timestamps for each detected event. She uses clinical software daily but has no audio analysis experience.

### User 29: Samuel
Samuel is a 33-year-old software developer integrating sound detection results into a research workflow. He wants to access detected event labels, start times, and end times in a structured format. He needs a consistent CSV or JSON export so that other programs can read the results without manual transcription. He is proficient in Python, APIs, and data processing.

### User 30: Emma
Emma is a 44-year-old EMS medical director reviewing a resuscitation case with a clinical team. She wants to use the detected event timeline to guide a discussion about what happened during ambulance transport. She needs to display important event categories, select specific time intervals, and replay the related audio while reviewing the case. She is comfortable with clinical dashboards and presentation tools but has no programming experience.
