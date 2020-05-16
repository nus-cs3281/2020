### Project: [Source Academy Cadet Frontend](https://github.com/source-academy/cadet-frontend)

The Source Academy is a gamified platform used in NUS's introductory programming module for Computer Science Freshmen, CS1101S. It is designed to teach students coding in a fun and interactive manner. The Cadet Frontend in particular houses the source code for the frontend written in ReactJS with Redux.

### My Contributions

I worked on improvements to the sound library for the Source Academy. 

These are my merged PRs:
- [Sound Improvements](https://github.com/source-academy/cadet-frontend/pull/520)
- [Fix Misc Sound Bugs](https://github.com/source-academy/cadet-frontend/pull/845)
- [Add Display Waveform Function](https://github.com/source-academy/cadet-frontend/pull/849)
- [Remove Duplicates Present in Both sounds.js And soundToneMatrix.js](https://github.com/source-academy/cadet-frontend/pull/928)
- [Add Early Return For Zero Duration Sounds](https://github.com/source-academy/cadet-frontend/pull/932)

#### Performance Issues

The sound library suffered heavily from performance issues. For more advanced assignments, students often had to wait upwards of 10 minutes between pressing "run" and hearing the actual sound played.

This was solved by reimplementing sound processing and removing redundant, computationally expensive operations.

#### New Features

Some new features implemented include:
- Microphone input capture and subsequent manipulation and playback
- Sound waveform visualisation
- Instantaneous playback of sounds (experimental feature)

### My Observations

#### Wiki For Specific Sub Projects

Source Academy developers maintain a wiki page for each sub-project or library which details the features, developer-relevant details and future plans or current limitations for the project.

This makes it easier for newer developers to get an idea for what each sub-project is about, its current state, and which areas need more work.

#### Issue Tracker Management
Unlike PowerPointLabs, the issue tracker for the Source Academy does not automatically generate an issue template for new issues. This could be an area of improvement for them as an issue template would ensure that all the relevant details are included when creating a new issue.

### Suggestions for PowerPointLabs

#### Wiki For Specific Labs
Taking a page from the Source Academy, it would be beneficial to have the developers for each lab to maintain a wiki topic to help new developers get acquianted with their lab.

It can also serve to document future plans or current limitations.
