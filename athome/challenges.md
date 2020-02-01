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
  - at current moment, the robotics field is not mainstream and hence identifying performant libraries are an art of itself
  - many existing off-the-shelve code are research code and hence requires expert knowledge in the field to use it, e.g., a user needs to see through undocumented assumptions and limitations
- lacking robotics systems engineer
  - difficult to find generalist robotics engineer
- developing a robotics system with underspecified requirements / task descriptions is challenging
  - the competition organizers or product managers do not have experience with describing the robotics problems precisely (due to lack of the experience in the field as a whole)

### Ops

- testing is hard
  - setting up a real world testing environment is challenging, esp, challenging to prepare the "reset"
  - the simulators do not serve the purpose they are designed for
    - inaccuracy - the gap between simulation and reality is too big
    - setting up and running experiments in simulation is too cumbersome
  - not enough time for thoroughly testing

- difficult to identify what is important and fail to allocate to time optimally, which often only becomes clearer after the project is over
  - so it is easy to get stuck on a not-important issue
- existing dev-ops tools are unfit for the robotics dev culture
  - no ROS binding, no real-world continuous testing, no robotics data focused data logging/analysis/visualization options ...

## Human-factor

- knowledge concentration problem - each team member knows their part thoroughly but do not know others' part and violates
- running the whole system is not practiced enough
  - mostly due to the time requirement of doing so
  - the importance of this practice is overlooked among inexperienced teams

## Structural

-
