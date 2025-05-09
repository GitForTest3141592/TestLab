---
layout: splash
title: SimPla - Simulated Plasma
permalink: /SimPla/
---

EQUILIBRIUM SOLVER

If you need to solve a plasma equilibrium problem, open Main_equilibrium.m.

EXAMPLE 1: SOLVE AN ITER-LIKE CONFIGURATION

First steps require to define essential geometrical and plasma parameters of your configuration.

All geometrical parameters are collected in a structure called “Geo”. In Main_equilibrium.m, we define first two geometrical parameters: 

major radius: Geo.R0 = 6 [m]

minor radius: Geo.a = 2 [m] 



All plasma equilibrium parameters are collected in the structure “Equi”, more specifically in its substructure “Equi.Config.param”.

Open Equilibrium_boundary.m, where you can input desired parameters through the function Equi_type_Jt_I_Config.m or by uploading your own file containing all data.

So, let’s now open Equi_type_Jt_I_Config.m.

First plasma equilibrium parameters are related to the desired plasma shape (for a better understanding, please refer to Appendix A), and they are:

upper elongation: Equi.Config.param.k1 = 1.7

lower elongation: Equi.Config.param.k2 = 2

upper triangularity: Equi.Config.param.d1 = 0.5

lower triangularity: Equi.Config.param.d2 = 0.5

upper inner angle: Equi.Config.param.gamma_n_1 = 0 [radians]

lower inner angle: Equi.Config.param.gamma_n_2 = pi/3 [radians]

upper outer angle: Equi.Config.param.gamma_p_1 = 0 [radians]

lower outer angle: Equi.Config.param.gamma_p_2 = pi/6 [radians]

Other parameters are related to the plasma current profile and magnetic field:

total plasma current Equi.Config.param.Ip = -10e6 [A]

plasma profile coefficient β0: Equi.Config.param.beta0 = 0.5

plasma profile coefficient α1: Equi.Config.param.alpha1 = 2

plasma profile coefficient α2: Equi.Config.param.alpha2 = 2

toroidal magnetic field on axis: Equi.Config.param.Bt0 = 5;

And lastly, parameters related to the numerical solver:

Maximum number of iterations: Equi.Config.param.Max_iter = 30

Stop condition on convergence error: Equi.Config.param.Error_conv = 1e-5



Now, return to Main_equilibrium.m and run the code.

