Q: What were the hardware-related problems?
---

- FSM launch file; 4-5
  - almost all teams
  - containers

- Software stack
  - hardware
  - driver
  - ROS nodes (action)
  - FSM
  - human interface

- Hardware
  - xtion 3D camera, playstation eye (for micro)
    - the ROS launch file on the docker file starts the hardware
    - sysbot
    - USB bandwidth

  - if hand slam
    - cable slips
    - TRI to retie

  - hot unplug power system

  - screen issues
    - display things that prompt

  - magnets
    - safe keep out magnets
    - Hall effect - motherboard e-stop

- very predictable, US floors were conduits

Q: What were the driver-level problems?
---

- HSR case
  - little visibility
  - all sort of reasons
  - unpredictable
  - no way to talk to the motors directly
    - interface to ROS was everything
    - no access

  - head behavior for get depth data to have a good test map

  - weird issues:
    - square maps pgm file; crop them and crash

  - Toyota - things that we did not write

  - things we wrote - many other issues
    - only appeared at robocup

  - smash => lifting into smash state

  - rospy / roscpp =>
    - always fail 2nd time you call
    - double wrapped-action to call twice in robocup; so only then they found out about the problem
  - why did you double (ros-)wrapped certain code?
    - tricky part: ROS has resources, process level access, e.g., working with environmental variables, etc.

---

- necessary frequency
  - very high requirement
  - task requirement is higher

- FSM bugs
  - mechanical engineers
  - fail to anticipate failure
  - mechanical level at this layer
    - how to share resources between states
      - information as dictionary (resources)
    - arm wrapper =>
  - thousands the subscribe
  - library provide suggestions; we not understand, wrong choices.

- people
  - launch file
  - tmux (villa)
  - don’t write launch file
  - tmux launcher

- Launch file writing is hard
  - multi-computer configuration problem

---


- human factor; people level
  -

- code / interface to developer
  - we can win with the tool
  - effectively on the robocup side

- soccer team had mature tool for

- HSR
  - drag binary over
    - dynamic linking
    - library again link against (slightly different API)
      - shipped Toyota
  - install space

- login & create their user account
  - easiest way to do with robot - because it has every


---

Towards modular architecture

- GPU & Cameras getting better and better
  - Combinatorial optimization problem of designing the

- Hardware space which leads to optimization problem

---

Thoughts on solutions

- follow

- use research code judiciously

- make testing easy

- why is setting up gazebo & image => gazebo problem hard?
  - computer problems
  - hard to run PCL code AND gazebo code (on my desktop)
  - need to find images, etc.

- diving up the system
  - somewhere between RL (opengym, too hard, also there some gap) & human-sim (Chao’s thing easy to build but miss things)
  - something in-between? using synthesizer to make creating test cases easier?

  - modeling the generative model of detector
    - simplest thing - remembering

- thought about building ROS<->XXX bridges using synthesizer

- testing closed-loop controller is hard because you need environment
  - for HRI there is subjective metric, too.

- grasping silverware problem
  - how can one model it? At abstract level?
