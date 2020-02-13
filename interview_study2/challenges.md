# Identified Challenges

Here is an initial list extracted from the [interview notes](./rawdata.md):

- working with immature (and rapidly changing/improving) software and hardware
  - immotile hardware setup
  - endless restarts

- working with black box software
  - unexpected behaviors and incomprehensible errors from proprietary sensor or actuator devices or drivers
  - working with vendors is time-consuming

- unintended use of software frameworks
  - causes efficiency and scalability issues
  - integrating multiple systems in a way goes beyond their spec limitations
  - due to lacking solutions for the problem at hand

- unintended use of hardware devices
  - every robotics tasks feel one-off

- orchestrating and operating a large number of tightly connected components

A list of questions for root cause analysis:

- why do roboticists rely on 3rd party software and hardware?
- why do roboticists integrate multiple frameworks?
- why do roboticists use multiple hardware devices?
- why are do the tasks feel one-off?
- what makes the testing hard?

Observed "tensions":

- The tension between using a "general" solution vs. devising one-off solution
  - "general" solutions are hard to set up, often does not work for your problem
  - the one-off solutions are not scalable
- The tension between committing early (aiming for a robust & tested system with known limitations) vs. keeping doors open (aiming to find the perfect fit)

Starter questions for solution brainstorming

- What will allow the roboticists to experiment more without breaking the existing system based on large, tightly connected components?
- What will allow the roboticists to spend more time on new-task or edge-case testing?
- Where are the changes likely to occur? Is modeling the likely changes possible? e.g., to (automatically) adjust the impacted components?
