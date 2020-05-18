### Project: Source Academy

[**Source Academy**](https://github.com/source-academy) is a website that facilitates the teaching of the CS1101S course in NUS. The programming course is conducted using a programming language called [Source](https://sicp.comp.nus.edu.sg/source/), a subscript of Javascript. The website provides the following features:

- Hosts a playground editor that allows users to play with the Source language
- Provides assessments that require the use of the Source language to complete

### My Contributions

- Added notification system to notify students of new assessments
  - [Frontend](https://github.com/source-academy/cadet-frontend/pull/656)
  - [Backend](https://github.com/source-academy/cadet/pull/407)
- Improve autograder system for finer granularity
  - [Frontend](https://github.com/source-academy/cadet-frontend/pull/568)
  - [Backend](https://github.com/source-academy/cadet/pull/363)

### My Observations

#### Development

Source Academy is a small project that encourages experimentation and learning, and hence allows year 1 students to contribute to Source Academy. There is not many requirements in the maintainance of the project, and contributors are free to develop new features without the stress or worry of meeting standards.

In contrast, CATcher is a simpler application that focuses on delivering a service for a crucial assessment in the CS2103/T module. 

#### Testing

Source Academy recommends unit tests to be written for new features that are developed. 

On the frontend, tests are written with Jest.

On the backend, tests are written with ExUnit.

#### Recommendations

CATcher can benefit from having more unit tests and integration tests. This ensures that CATcher does not suffer from regression issues if we seek to develop new features or experiment with the application more.