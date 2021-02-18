# AI & Drone Control 
This open book is about applying AI techniques (machine learning, deep learning and reinforcement learning) to drone control systems. 

## Control
Everything is Model-based: Model-based Cotnrol and Model-based Reinforcement Learning. 

Models are built in Matlab & Simulink. Experiments are run in simulator and on a real Parrot Mambo drone. 

### Optimal control vs Robust control
Optimal control assumes the model is perfect while Robust control assumes the model is imperfect. This book focuses on Robust control applications on drones. 

### Robust Control
A successfully designed control system should be always able to maintain a stability and performance level in spite of uncertainties in system dynamics and/or in the working environment to a certain degree. 

Robust control can only be achieved by a closed-loop (or feedback) system, which uses sensors to measure the actual output to adjust the input in order to achieve desired output. The drone system we are interested in is a linear, time-invarian, continuius time, multivariable feeback system. 

#### Uncertainty
Uncertainties are unavoidable in a real control system. The uncertainty can be classified into two categories: disturbance signals and dynamic perturbations. The former includes input and output disturbance (such as a gust on an aircraft), sensor noise and actuator noise, etc. The latter represents the discrepancy between the mathematical model and the actual dynamics of the system in operation. 

A mathematical model of any real system
is always just an approximation of the true, physical reality of the system dynamics. Typical sources of the discrepancy include unmodeled (usually high-frequency)
dynamics, neglected nonlinearities in the modeling, effects of deliberate reducedorder models, and system-parameter variations due to environmental changes and
torn-and-worn factors. 

#### Problems
Disturbance  signals / Noise interference / Unmodeled plant dynamcis / Drone parameter variations

#### Solutions
H∞

# References

Robust Control Design with MATLAB®, 2nd edn. Springer

[Brian Douglas](https://engineeringmedia.com/videos)

[Steven L. Brunton](https://www.youtube.com/watch?v=oulLR06lj_E&list=PLMrJAkhIeNNQkv98vuPjO2X2qJO_UPeWR)
