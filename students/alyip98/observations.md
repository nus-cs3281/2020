### Project: Text-to-Image

[Text-to-Image](https://github.com/bostrom/text-to-image) is a library for generating an image data URI representing an image containing the text of your choice. It supports a large variety of options, such as font size, font family, color, rotation, custom margins/kerning. The library exposes a single function that parses all those options and converts the supplied text to an image.

### My Contributions

- Add a synchronous variant of the library's main function [PR](https://github.com/bostrom/text-to-image/pull/34)

The existing implementation is a Promise based async function, which cannot be used in a sync rendering flow, such as in the plugin rendering context of Markbind. After understanding the project code, I was able to cleanly refactor the existing code to separate the core logic from the function entry point, which allowed me to implement a synchronous variant of the same function with minimal duplicated code. 

### My Observations

#### Good User Documentation
The user facing documentation is very well written. It is clear and easy to understand, containing just enough examples to illustrate its use without being verbose. We could adopt this approach in our internal projects, 

#### Comprehensive Test Coverage
This project has a 100% code coverage using Jest. In this case it is feasible and practical as it is a small project, but I think the spirit of it could be reproduced in our internal projects. The comprehensive arsenal of unit tests check for everything imaginable, including an interesting test where a few pixels of the generated image was checked. If we haven't already, Markbind could look into tests that employ a similar screenshotting method to augment our diff checks.

