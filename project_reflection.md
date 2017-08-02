### Project Refection on PID Control Project
---
**Describe the effect each of the P, I, D components had in your implementation.**
- P component is the main parameter to correct the steering angle depends on the CTE. When P is large it will steer with large angle to steer back to the track, however in the most of the cases, it will overshoot. Eventually, it will oscillate without an end. With small P, it will not respond rapidly. 
- I component is the parameter to reduce CTE to zero, a proper choice of I parameter can reduce error even when there is sensor drifting occurring. 
- D component is the parameter to compensate the rapid change in CTE error. It reduce the change of overshoot or oscillation. 

**Describe how the final hyperparameters were chosen**
Finaly hyperparameters choice:

**P = -0.5**
**I = -0.001**
**D = -0.9**

**P** was set to -0.5 initially, however it overshot after the simulation ran. Then a smaller value of **P = -0.1** was choosen. The result was better than before, however it overshot eventually. Then **D = -0.5** was choosen as another parameter to steer the car at the center of the track. However the overshooting situation was delayed compared to before. It was not satisfied. It seemed that the steering angle was still changing too rapidly thus, a larger value of **D = -0.9** was chosen. Result looked better than before. For **I** parameter, there is no evidence that the CTE error will build up rapidly over time, therefore a small value of **I = -0.001** was choosen.
