# Identified Challenges

## Technical

- manipulation
  - bi-hand
  - general manipulation that does not require strong assumptions
- human-in-the-loop control
  - modeling humans at multiple levels
- integration
  - multiple robotics concepts
  - multiple software/hardware platforms


## Engineering

### Dev

- lack of performant off-the-shelve tools
  - identifying performant libraries is an art of itself
  - many existing off-the-shelve code is research code
    - it requires expert knowledge in the field to use available research code, e.g., a user needs to see through undocumented assumptions and limitations
- lacking robotics systems engineer
  - difficult to find generalist robotics engineer
- underspecified requirements / task descriptions
  - it is challenging (for competition organizers or product managers) to describe robotics tasks precisely
- a large and diverse system
  - makes it difficult to identify the high priority tasks and hence it is hard to allocate to time optimally, which often only becomes clearer after the project is over

### Ops

- existing dev-ops tools are unfit for the robotics dev culture
  - no ROS binding, no real-world continuous testing, no robotics data focused data logging/analysis/visualization options ...
- testing is hard
  - setting up a real-world testing environment is challenging, esp, challenging to prepare the "reset"
  - the simulators do not serve the purpose they are designed for
    - inaccuracy - the gap between simulation and reality is too big
    - setting up and running experiments in simulation is too cumbersome
  - real-world testings take too long time
  - designing the testing cases that cover the specs "just enough" is an art
    - the team often misses the important test cases or not test the important cases thoroughly enough


## Misc

- knowledge concentration problem
  - each team member knows the component they own thoroughly but do not know those of others
- human-factor is overlooked
  - many human error occurs while running the whole system
  - related to the knowledge concentration problem and the testing challenges
