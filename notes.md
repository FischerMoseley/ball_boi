Ideas for types of control:
- LQR
- iLQR
- machine learning -> Jorge 
- not dynamic programming
- guess a Lyaponuv function
- constraint programming + trajectory optimization (give it a guess and some constraints)

We need to:
- come up with a metric for comparing models (max degree off-center to stabilize, time needed to stabilize)
- control it lol

For Project Update #1:
- person with LQR should do some performance characterization -> Fischer
- Suzanna -> attempt optimization (initial guess = LQR?)

Extra:
- give it complicated terrain (like a halfpipe)
- least time controllers (can you run faster with optimization than with LQR?), constrain motor torque + tilt angle

Jorge's machine learning:
- can (1) solve for optimal controller or (2) solve a cost function and use cost func to eval optimal controller


For the report:

- we have LQR, traj control, neural net in 2D
- we want to change the plant to see how robust these controllers are
  
  possible adjustments: change in mass, actuator limit (that controller was unaware of), joint offsets?, disturbances
  
  more difficult one would be distubances -> add noise to state variables
  
- we can make these changes and analyze why we chose these
- traj optimizer with iLQR (currently open-loop), would redefine LQR at each time step
- need functions to evaluate:

    integrated cost (ie. total cost it took to get there), can break up by state (away from target state) and actuation state -> quad cost function
    
    time to steady state (ie. settling time)
    
    overshoot
    
    average tilt angle
    
- stability as a function of 4 DOF for initial conditions (x, xdot, theta, thetadot)
- maybe need to try and integrate a cost function into the trajectory optimization
- can try asking traj optimizer to never overshoot
