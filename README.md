# The Practice of Android @ OCTanner
This is how we work and live our craft.

## Onboarding of New Developers
> We follow [the onboarding of new developers](./guidelines-new-onboard-resource.md) process to enable new developer to start productive work swiftly.
## Code Reviews

> We use Github Pull Requests to drive face-to-face code reviews by following [code review checklist](./code-review-checklist.md). We expect everyone to submit pull requests every day or two at the least. One team member is assigned to conduct all code reviews on a given weekday.

We believe that code reviews are an essential tool for keeping code quality high. Everything we do gets code reviewed. We use Github, and have pull requests be the only way that code gets into our repository. We have a more detailed document showing all of the steps of our code reviews, but the essentials include a face-to-face review of the code, and an expectation that we will discuss both style and approach, in addition to syntax, structure, and other mechanics.

## Coding Style

> We follow AOSP Java Code Style for android java code and our [O.C. Tanner style guide for android code](./style-guide.md). Any deviations are specified in our style guide amendments.

We believe the best way to keep code readable among a team is to establish a us set coding style. Obviously such a style will involve compromises, but the outcome is worth the effort when everybody can read code written by others.

## Testing

> We use Android Testing Support Library, provides a set of APIs that allow you to quickly build and run test code for your apps, including JUnit 4 and functional UI tests. The library includes the following instrumentation-based APIs that are useful when you want to automate your tests:
                                          
    AndroidJUnitRunner
        - A JUnit 4-compatible test runner for Android.
    Espresso
        - A UI testing framework; suitable for functional UI testing within an app.
    UI Automator
        - A UI testing framework suitable for cross-app functional UI testing between both system and installed apps.

We believe testing is an essential tool for developing reliable code and keeping it in shape to allow for confidently making changes to our code in the future.

## Logging

> We treat logs as data and use a structured logging format for all logs.

We believe logging enhances our understanding of the runtime characteristics of our applications and provides an invaluable tool in finding bugs in our applications. We use it as a complement to the debugger when locating the source of errors.

## Learning

> We do on-the-job learning.

We believe that each of us has room to grow, and that taking time to learn is essential to providing our employer with the very best quality code.

## Community

> We participate in the Android community by both learning and giving back to it.

We believe that in being a strong part of our local community, we help lift all of us in our desire to be the best programmers we can be.