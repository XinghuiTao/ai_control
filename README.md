# AI & UAV Control 
This open book is about applying AI techniques (machine learning, deep learning and reinforcement learning) to UAV control systems. 

## Model-based Desgin
Model-based design provides an efficient approach for establishing a common framework for communication throughout the design process while supporting the development cycle (V-model). In model-based design of control systems, development is manifested in these four steps:

    modeling a plant,
    analyzing and synthesizing a controller for the plant,
    simulating the plant and controller,
    integrating all these phases by deploying the controller.

## Control
Everything is Model-based: Model-based Cotnrol and Model-based Reinforcement Learning. 

Models are built in Matlab & Simulink. Experiments are run in simulator and on a real Parrot Mambo drone. 

### Optimal control vs Robust control
Optimal control assumes the model is perfect while Robust control assumes the model is imperfect. This book focuses on Robust control applications on UAVs. 

### Robust Control
A successfully designed control system should be always able to maintain a stability and performance level in spite of uncertainties in system dynamics and/or in the working environment to a certain degree. 

Robust control is not one controller but a design method. Robust cotrol addresses uncertainty. 

Robust control can only be achieved by a closed-loop (or feedback) system, which uses sensors to measure the actual output to adjust the input in order to achieve desired output. UAV systems are a linear, time-invarian, continuius time, multivariable feeback systems. 

A mathematical model of any real system is always just an approximation of the true, physical reality of the system dynamics. Typical sources of the discrepancy include unmodeled (usually high-frequency) dynamics, neglected nonlinearities in the modeling, effects of deliberate reducedorder models, and system-parameter variations due to environmental changes and torn-and-worn factors. 

#### Problems
##### Uncertainty
Uncertainties are unavoidable in a real control system. The uncertainty can be classified into two categories: disturbance signals and dynamic perturbations. The former includes input and output disturbance (such as a gust on an aircraft), sensor noise and actuator noise, etc. The latter represents the discrepancy between the mathematical model and the actual dynamics of the system in operation. They can be caused by complex dynamics(high frequency), uncertain driving forces(gust), intentional simplicity(linearalisation), stochastic events(torn-and-worn), process variations(production).

"I don't know everything (model and/or disturbance) perfectly, but I'm confident it's going to work!" (Brian Douglas)

##### MIMO



#### Aanlysis
##### Margin
Margin is a way to specify how much uncertainty your system can hangle before it no longer meets the requirement. 

##### Disk margin
The disk margin measures how much uncertainty the loop can tolerate before going unstable. That uncertainty amount corresponds to minimum gain and phase margins. The disk-based gain margin (DGM) is the amount by which the loop gain can increase or decrease without loss of stability, in absolute units.

```Matlab
L = tf(25,[1 10 10 10]);
[DM, MM] = diskmargin(L, 0);
DM = 
GainMargin: [0.6273 1.5942]
PhaseMargin: [-25.8017 25.8017]
DiskMargin: 0.4581
LowerBound: 0.4581
UpperBound: 0.4581
Frequency: 1.9550
WorstPerturbation: [1×1 ss]
```
<img src="https://github.com/Tao-wecorp/ai_control/blob/main/img/disk_margin.png" height="100" />

https://zhuanlan.zhihu.com/p/148966504

### Solutions
The H∞ optimization approach and its related approaches have been shown to be effective and efficient robust design methods for such control systems.

# References

Robust Control Design with MATLAB®, 2nd edn. Springer

[Brian Douglas](https://engineeringmedia.com/videos)

[Steven L. Brunton](https://www.youtube.com/watch?v=oulLR06lj_E&list=PLMrJAkhIeNNQkv98vuPjO2X2qJO_UPeWR)
