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
