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

- necessary frequency were dependent on nodes
  - very high requirement
  - task requirement is higher

Q: What were the robot behavior-level problems?
---

- FSM bugs
  - small mistakes introduced by a mechanical engineer
  - "fail to anticipate failure" type
  - mechanical level at this layer
    - how to share resources between states
      - information as dictionary (resources)
    - arm wrapper were not meant to be "resource"
  - thousands subscriptions to a topic (due to the FSM expansion) - ROS could not handle that
  - library provide suggestions; we not understand, wrong choices.


Q: What were the human operator-level problems?
---

- chance in people's behavior:
  1. launch file
  2. tmux
  3. don't write launch file
  4. tmux launcher

- Launch file writing is hard
  - the multi-computer configuration problem

- code & interface to developer
  - we can win with simpler tools
  - effectively on the robocup side

- soccer team had mature tool for deploying new code

- HSR
  - drag binary over
    - dynamic linking caused problems
    - the library had slightly different API between the desktop & the robot computer
      - the comptuer shipped from Toyota
  - install space

- login & create their user account
  - easiest way to do with robot - because it has everything setup

Q: Anything else?
---

Towards modular architecture

- GPU & Cameras getting better and better
- space for putting hardware devices is limited
