# ACMSIMC_TUT
> AC Machine Simulation in C (Tutorial Version)

## Introduction
I have used C to simulate motor control and adptive observers for over 4 years now.
This is a tutorial for those who hate using Simulink to simulate ac motor control.
The benefit is that you can direct reuse the codes in DSP based motor drive.

## Numerial Methods
The numerical integration method is currently RK4, which is quite enough. 
DoPri54 will be included in future version (including stiffness detection and variable step numerical integration).

## Introduction to Current Branches:
- [IM] master: combination of other branches, kept in a developing status in which I feel good.
- [IM] vvvf: the skeleton with induction motor simulation and VVVF control.
- [IM] foc: field oriented control (direct/indirect) with basic sensorless control.
- [IM] animate: test the feature of waveform (results) animation.
- [PMSM] pmsm: id=0 control for interior permanent magnet synchronous motor.
- [IM] vi_decouple: add voltage-current decoupling circuit for improved control performance during high speed reversal.
- [IM] mras: model reference adaptive system based sensorless control (my 2017-Chen.Huang-Online paper).
- [IM] \_femm: (This branch does not really belong here but I don't want to create a new repository for it...) It is about the design of the induction motor using free softwares as well as fitting the design to the equivalent circuit parameters for further control simulation.
- [IM] saturation: include iron core saturation effect into the induction motor model simulation.
- [Both] inverter_model: simple inverter modeling based on the paper 1996-Choi.Sul-Inverter.

## Visualization
- The plots are made using package matplotlib. 
    - In branch animate, I tested the feature of waveform animation with matplotlib.
- You can also try browser based libraries, e.g., plotly_express.

## Dependency under Windows
- Anaconda 3 (you should be able to call python from cmd.exe)
- MinGW (you should be able to call gcc from cmd.exe)
- FEMM ([femm.info](http://www.femm.info/wiki/HomePage), you do not need this if you are not interested in Finite Element Analysis and motor design)
  - PyFEMM (a wrapper for FEMM API; use pip to install this)
- Editor (optional): Sublime Text (preferred) or Visual Studio Code.

## Dependency under Linux
- FEMM is a Windows-only FEA software. 
    - Alternative is ElmerFEM for Linux, but it is poorly documented. Please DO NOT try it out unless you are a ドM.
- Others are not tested yet. (Linux users should be able to figure it out...)

## Video Tutorials
For unfamiliar users, I have been creating video tutorials. However, they are currently in Chinese. 
In near future, tge Engligh version will be brought about.

> If you speak Chinese, I have a dedicated tutorial video on how to make this thing work from the ground up.
> Please take a look at this link to [知乎](https://zhuanlan.zhihu.com/p/64445558).
> In fact, now you can check out [my personal page](https://horychen.github.io) for a list of tutorial videos.

#################################Original Post Above

## Tiny 2020.02.08
TO DO List
1) Seperate Programm Functions into different python modules
2) GUI in QT
2.5) Async communications between Real-time and GUI module
3) design a python to c source translator(like simulink) (further plan)
4) motor topology
