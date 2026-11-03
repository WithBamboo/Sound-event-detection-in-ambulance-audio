Who is the user. What do they want to do with the tool. What needs and desires do they want for the tool. What is their skill level.

Take 20 mins to write at least 30 user stories in this format in the markdown file you just created. After a couple, flag an instructional team member for input before you write all 30. 

The doctor is user. They want to use this tool do understand what happens 

### User 1: Tom
Tom is a 50-year-old emergency physician receiving a patient after ambulance transport. He wants to locate and replay sections of the recording containing defibrillator charging sounds so that he can review when these sounds occurred during resuscitation. He needs clickable timestamps and short audio clips rather than having to listen to the entire recording. He is comfortable using graphical clinical software but has no command-line experience. 

### User 2: Mary
Mary is a 40-year-old cardiologist reviewing a 20-minute ambulance recording after a resuscitation. She wants to find possible pauses between detected CPR compression sounds without listening to the entire recording. She needs to filter the timeline to show CPR events, see the start and end timestamps of each detected interval, and click a possible gap to hear the audio immediately before and after it. She wants to check these clips herself because background noise may cause the tool to miss compression sounds. Mary uses graphical clinical software daily but has no programming or command-line experience.

### User 3: James
James is a 35-year-old paramedic reviewing an ambulance recording after a difficult emergency call. He wants to understand the sequence of resuscitation-related sounds during transport. He needs a chronological timeline showing detected CPR compressions, metronome tones, and defibrillator charging sounds, with different colors or labels for each event type. He regularly uses electronic patient care reporting systems but has no programming experience.

### User 4: Sarah
Sarah is a 42-year-old EMS training instructor preparing a CPR training session for new paramedics. She wants to find examples of consistent and interrupted CPR compression sounds from recorded ambulance scenarios. She needs to filter recordings by CPR events, select specific time intervals, and replay short audio clips during training. She is comfortable using presentation software and audio players but has no experience with Python or command-line tools.

### User 5: David
David is a 29-year-old emergency medical technician reviewing a recording after completing a patient transport. He wants to check whether metronome tones were consistently detected during a CPR session. He needs a timeline showing detected metronome events, possible gaps between them, and clickable timestamps to replay those intervals. He uses electronic medical records regularly but has limited experience with audio analysis software.

### User 6: Emily
Emily is a 38-year-old EMS quality improvement coordinator reviewing multiple emergency transport recordings. She wants to compare detected CPR and defibrillator-related events across different cases to identify recordings that may need further review. She needs a summary table showing event counts, event types, and timestamps for each recording, along with a CSV export option. She regularly uses Excel and reporting dashboards but has no programming background.

### User 7: Michael
Michael is a 26-year-old medical research assistant evaluating the accuracy of an ambulance sound detection model. He wants to compare automatically detected events with manually labeled audio segments. He needs to view predicted event labels and timestamps alongside reference annotations, replay the corresponding audio, and record incorrect predictions. He has basic Python and data analysis experience.

### User 8: Linda
Linda is a 45-year-old ambulance operations supervisor reviewing an emergency response recording. She wants to quickly locate possible defibrillator charging sounds without listening to the entire recording. She needs a searchable event list with timestamps and direct links to the corresponding audio segments. She uses scheduling and reporting software daily but has no programming experience.

### User 9: Alex
Alex is a 24-year-old computer science student helping test an ambulance sound detection model. He wants to identify audio segments where sirens, conversations, or equipment noise may have been incorrectly classified as CPR or metronome sounds. He needs to review predicted labels, listen to the original audio, and flag false positives for further analysis. He is comfortable using Python, GitHub, and basic machine learning tools.

### User 10: Rachel
Rachel is a 33-year-old emergency department nurse receiving a patient from an ambulance team. She wants a quick overview of detected resuscitation-related sounds before reviewing the patient's transport information. She needs a simple event summary showing sound categories, approximate timestamps, and the chronological order of detected events. She uses electronic health record systems daily but has no programming experience.

### User 11: Kevin
Kevin is a 31-year-old paramedic completing a patient care report after an emergency transport. He wants to reference detected CPR compressions, metronome tones, and defibrillator charging sounds while reconstructing the sequence of events. He needs a chronological event list with timestamps and a way to copy or export the information into his documentation workflow. He is experienced with electronic patient care reporting systems but has no programming background.

### User 12: Olivia
Olivia is a 36-year-old emergency physician reviewing an ambulance recording containing overlapping equipment sounds. She wants to examine periods where CPR compressions and defibrillator charging sounds may have occurred close together. She needs multiple event categories displayed on the same timeline and the ability to zoom into a selected interval and replay the audio. She regularly uses clinical software but has little experience with audio analysis tools.

### User 13: Daniel
Daniel is a 27-year-old paramedic instructor reviewing a CPR training recording with students. He wants to compare detected compression sounds with metronome tones to discuss whether the compressions appear to follow the intended training rhythm. He needs both event categories displayed on a synchronized timeline and the ability to replay selected sections. He is comfortable with graphical training software but has no programming experience.

### User 14: Sophia
Sophia is a 30-year-old healthcare data analyst analyzing resuscitation-related sounds in ambulance recordings. She wants to understand the distribution of detected sound events within each recording. She needs a summary showing the number of detected CPR, metronome, and defibrillator charging events, along with a table of timestamps and a CSV export option. She regularly uses Excel and SQL and has basic Python experience.

### User 15: Brian
Brian is a 43-year-old EMS supervisor reviewing a 45-minute emergency transport recording. He wants to skip sections without relevant detected sounds and focus on periods containing resuscitation-related events. He needs an interactive timeline with event markers and controls that let him jump directly to each detected interval. He uses reporting and office software regularly but has no programming experience.

### User 16: Hannah
Hannah is a 25-year-old research assistant preparing an annotated ambulance audio dataset. She wants to correct event labels and timestamps when the detection model makes mistakes. She needs to listen to selected audio segments, change event categories, adjust start and end times, and save the corrected annotations. She is familiar with Python and basic audio annotation software.

### User 17: Robert
Robert is a 48-year-old EMS quality assurance manager reviewing possible interruptions in CPR during ambulance transport. He wants to locate intervals where CPR compression sounds were not detected for a relatively long period. He needs the tool to highlight possible gaps, display their durations, and allow him to replay the surrounding audio before determining whether an interruption actually occurred. He regularly uses clinical reporting applications but has no programming experience.

### User 18: Jessica
Jessica is a 34-year-old emergency medicine researcher studying the timing of resuscitation-related sounds. She wants to examine how detected CPR compression events and defibrillator charging sounds are distributed throughout an ambulance recording. She needs event labels, start and end timestamps, and a structured CSV export for further statistical analysis. She has intermediate Python experience and regularly uses statistical software.

### User 19: Andrew
Andrew is a 39-year-old paramedic reviewing a recording with loud sirens, conversations, and equipment noise. He wants to identify detected events that may be less reliable because of background interference. He needs confidence indicators, when available from the model, and direct access to the corresponding audio so he can review uncertain detections himself. He uses clinical software regularly but has no machine learning background.

### User 20: Natalie
Natalie is a 28-year-old graduate student evaluating how background noise affects sound event detection. She wants to compare model predictions on recordings with different noise levels. She needs to upload audio files, inspect detected event timestamps, compare predictions with reference labels, and summarize differences in detection performance. She is comfortable with Python, data visualization, and basic machine learning.

### User 21: Peter
Peter is a 52-year-old emergency physician reviewing ambulance recordings between patient consultations. He wants to quickly understand which resuscitation-related sounds were detected without listening to the full recording. He needs a concise summary showing event categories, counts, and approximate timestamps, with an option to open individual audio segments when necessary. He regularly uses electronic medical record systems but has no programming experience.

### User 22: Grace
Grace is a 32-year-old EMS training coordinator preparing educational materials from recorded emergency scenarios. She wants to save examples of CPR compression, metronome, and defibrillator charging sounds for training discussions. She needs to select a time range around a detected event, preview the audio, and export the selected clip as a separate file. She regularly uses presentation and basic video editing software but has no programming background.

### User 23: Ethan
Ethan is a 23-year-old computer science student testing the ambulance audio detection application. He wants to check how the system handles valid recordings, unsupported file formats, and failed analysis attempts. He needs clear upload progress indicators, error messages explaining why a file cannot be processed, and confirmation when analysis is completed. He has experience with Python and basic software testing.

### User 24: Victoria
Victoria is a 41-year-old hospital quality improvement specialist reviewing multiple ambulance recordings. She wants to identify cases containing unusually long intervals without detected CPR compression sounds. She needs to compare possible gap durations across recordings, filter cases by a selected duration threshold, and open the relevant audio sections for manual review. She regularly uses Excel and clinical reporting dashboards but has no programming experience.

### User 25: Chris
Chris is a 37-year-old ambulance paramedic working on a shared computer after an emergency call. He wants to upload and analyze an audio recording without installing Python or additional software on the workstation. He needs a browser-based interface with an upload button, clear processing status, and an accessible event timeline. He regularly uses web applications but has no command-line experience.

### User 26: Mia
Mia is a 29-year-old biomedical engineering researcher studying overlapping sounds in ambulance recordings. She wants to understand cases where CPR compression sounds overlap with speech, sirens, or vehicle noise. She needs to examine short audio segments, inspect predicted event labels and timestamps, and compare predictions with manually verified annotations. She has experience with Python, signal processing, and machine learning.

### User 27: George
George is a 46-year-old EMS operations manager preparing a summary report across several emergency transport cases. He wants to compare the frequency of detected resuscitation-related sound events across recordings. He needs a table listing each recording, the number of detected events by category, and a CSV export that can be opened in Excel. He is experienced with spreadsheets and business reporting software but has no programming background.

### User 28: Lily
Lily is a 27-year-old emergency department nurse reviewing an ambulance recording during a patient handoff. She wants to distinguish CPR compression sounds from metronome tones and defibrillator charging sounds without studying the underlying detection model. She needs clearly labeled categories, distinct visual markers, and timestamps that are easy to understand at a glance. She uses clinical software daily but has no experience with audio processing or programming.

### User 29: Samuel
Samuel is a 33-year-old software developer integrating ambulance sound detection results into a research pipeline. He wants to automatically process the output of the detection tool without manually copying information from the interface. He needs a consistent CSV or JSON format containing event categories, start and end timestamps, and recording identifiers. He is proficient in Python, APIs, and data processing.

### User 30: Emma
Emma is a 44-year-old EMS medical director conducting a case review with a clinical team. She wants to use detected sound events to guide discussion of the sequence of activities during ambulance transport. She needs a timeline showing relevant event categories, the ability to select specific intervals, and audio playback for reviewing important moments with the team. She is familiar with clinical dashboards and presentation tools but has no programming experience. 
