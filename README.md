# AI & UAV Control 
This open book is about applying AI techniques (machine learning, deep learning and reinforcement learning) to UAV control systems. 

## Control
Everything is Model-based: Model-based Cotnrol and Model-based Reinforcement Learning. 

Models are built in Matlab & Simulink. Experiments are run in simulator and on a real Parrot Mambo drone. 

### Optimal control vs Robust control
Optimal control assumes the model is perfect while Robust control assumes the model is imperfect. This book focuses on Robust control applications on UAVs. 

### Robust Control
A successfully designed control system should be always able to maintain a stability and performance level in spite of uncertainties in system dynamics and/or in the working environment to a certain degree. 

Robust control can only be achieved by a closed-loop (or feedback) system, which uses sensors to measure the actual output to adjust the input in order to achieve desired output. UAV systems are a linear, time-invarian, continuius time, multivariable feeback systems. The H∞ optimization approach and its related approaches have been shown to be effective and efficient robust design methods for such control systems.

A mathematical model of any real system is always just an approximation of the true, physical reality of the system dynamics. Typical sources of the discrepancy include unmodeled (usually high-frequency) dynamics, neglected nonlinearities in the modeling, effects of deliberate reducedorder models, and system-parameter variations due to environmental changes and torn-and-worn factors. 

#### Problems
Uncertainties are unavoidable in a real control system. The uncertainty can be classified into two categories: disturbance signals and dynamic perturbations. The former includes input and output disturbance (such as a gust on an aircraft), sensor noise and actuator noise, etc. The latter represents the discrepancy between the mathematical model and the actual dynamics of the system in operation. They can be caused by complex dynamics(high frequency), uncertain driving forces(gust), intentional simplicity(linearalisation), stochastic events(torn-and-worn), process variations(production).

"I don't know everything (model and/or disturbance) perfectly, but I'm confident it's going to work!" (Brian Douglas)

#### Solutions
##### Add margin (Classical gain and phase margin)
1. Too liyyrt, or applied in the wrong spot = failed requirement
2. too much, or overly conservative = more expensive control system

# References

Robust Control Design with MATLAB®, 2nd edn. Springer

[Brian Douglas](https://engineeringmedia.com/videos)

[Steven L. Brunton](https://www.youtube.com/watch?v=oulLR06lj_E&list=PLMrJAkhIeNNQkv98vuPjO2X2qJO_UPeWR)
