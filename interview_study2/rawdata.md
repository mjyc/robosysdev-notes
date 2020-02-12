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
    - the ros launch file on the docker file starts the hardware
    - sysbot
    - USB bandwidth

  - if hand slam
    - cable slips
    - TRI to retie

  - hot unplug powersystem

  - screen issues
    - display things that prompt

  - magnets
    - safe keep out magnets
    - Hall effect - motherboard e-stop

- very predictable, US floors were conduit

---

- HSR case
    - little visibility
    - all sort of reasons
    - unpredictable
    - no way to talk to the motors directly

      - interface to ROS was everything

    - no access

    - head behavior for get depth data to have a good test map

    - ppm
      - square maps pgm file; crop them and crash

    - Toyota - things that we did not wright

    - things we wrote - many other issues
      - only appeared at robocup

    - smash => lift into smash state

    - rospy / roscpp =>
        - always fail 2nd time you call
        - double wrapped action to call twice in robocup; so only then they found out

     - why did you do double wrapping
         - tricky part: ROS has resources, process level - ports to get information | initialize PORT etc.

---
