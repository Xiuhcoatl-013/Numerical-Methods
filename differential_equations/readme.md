```html

<!--
-->
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<meta name="description" content="Numerical Methods [Real Time and Embedded Systems Programming]">
<meta name="keywords" content="DocOnce,computer program,programming,language programming,language computer,MATLAB,Octave,Fortran,C,C++,Python,Maple,Mathematica,syntax,bug,debugging,script (and scripting),algorithm,execute (a program),implement (a program),bug,debugging,simulation,model mathematical,print,program run,program execute,code,comment,instruction,program statement,variable,assignment,calculator,text editor,Emacs,Vim,Gedit,Notepad++,TextWrangler,Spyder,Python  installation,IPython,prompt,program typing,program run,program execute,function,function call,atan,function input parameter,function output parameter,function return,function take a parameter,library,library function,from,module,package,NameError,WARNING,import  math,math,plot,numpy,import numpy,matplotlib.pyplot,import matplotlib.pyplot,linspace,xlabel,ylabel,plot,array,interactive use (of Python),keyboard arrow up/down,prompt,Python shell,IPython,import,operator Arithmetic,parentheses,rounding error,variable type,variable name,object,float,int,str,type conversion,reserved words,variable int,variable float,variable str,variable assignment,type conversion automatic,integer division,rounding error,printing formatted,printf formatting,default,array,array element,zeros,allocate,array index,indexing zero based,indexing one based,Python zero-based indexing,array slice of,copy,graph,hold (on/off),plot figure,title (plot),legend (plot),axis (plot),hardcopy (plot),format png,matrix mat,transpose (of matrix),matrix vector product,linear algebra,matrix,vector,error message,debugging,debugger,try-exception,exception handling,program crash,program testing,testing,program verification,verification,validation,list,tuple,raw input,program input,program output,input,symbolic computations,symbolic operations,symbolic simplifications,SymPy,library SymPy,WolframAlpha,Mathematica,Sage (symbolic package),variable delete,Python documentation,garbage collection,long lines (splitting of),fast code,commenting code,if,elif,else,colon,indent,boolean,boolean expression,True,False,boolean True,boolean False,pseudo code,random walk,random (function),import random (function),operator Logical,def,function,function definition,return,argument,parameter input,parameter output,main program,return value,variable local,variable global,argument keyword,argument named,argument ordinary,argument positional,doc string,function handle,function local,function global,function nested,lambda function,range,loop for,for loop,loop iteration,loop index,loop double,loop multiple,loop nested,linear algebra,while loop,loop while,loop infinite,loop iteration,loop index,stop program (Ctrl+c),list,list append,list convert to array,list delete,list create,tuple,list comprehension,read (from file),write (to file),loadtxt,savetxt,array sorting,Leibniz pi,Euler pi,programming game,linear interpolation,least squares method,Fourier series,integral analytically,integral exact,integral numerically,integral approximately,Trapezoidal rule,composite trapezoidal rule,integration points,implementation specific,implementation general,import module,module,test block,code re-use,flat program,program flat,error function (erf),Midpoint method,composite midpoint method,Simpson's rule,Gauss quadrature,bug,unit tests,testing procedures,convergence rate,rate of convergence,error asymptotic,finite precision (of float),floating point number (float),error rounding,error tolerance,difference absolute,difference relative,assert (function),function assert,nose (testing),py.test,test function,vectorization,computational speed (measuring),domain,double integral midpoint,double sum,code re-use,triple integral midpoint,domain,domain complex,domain,Monte Carlo integration,seed (random generators),dynamical system,scheme,differential equation first-order,model mathematical,model differential equation,model computational,exp math notation,finite difference method,mesh,mesh uniform,mesh points,forward difference approximation,difference forward,Forward Euler scheme,Euler's method,numerical scheme,demo function,logistic model carrying capacity,SIR model,compartment model,mathematical modeling,scalar ODE,ODE scalar,vector ODE,ODE vector,system of ODEs,asarray (function),function asarray,discontinuous coefficient,spring oscillations,spring damping of,differential equation second-order,simple pendulum,second-order ODE rewritten as two first-order ODEs,difference forward,difference backward,Heun's method,Runge-Kutta, 2nd-order method,2nd-order Runge-Kutta method,RK2,difference centered,nonlinear algebraic equation,Runge-Kutta-Fehlberg,Crank-Nicolson method,spring damping of,spring nonlinear,spring linear,scaling,resonance,Verlet integration,Crank-Nicolson method,Taylor series,PDE,heat equation,diffusion equation,source term,domain,initial conditions,boundary conditions,MOL forward Euler,method of lines,MOL,mesh points,cell,method of lines,class,closure,unstable solutions,instability,stability criterion,scaling,vectorization,tridiagonal matrix,matrix tridiagonal,theta rule,Poisson equation,Laplace equation,root finding,brute force method,code robust,divergence,code exception,code try-except,Newton starting value,sys.exit,exit (sys),return None,rate of convergence,Idle,Emacs,Vim,Gedit,TextWrangler,Notepad++">

<title>Numerical Methods [Real Time and Embedded Systems Programming] Differential Equations</title>

<!-- Bootstrap style: bootswatch_journal--> 
<!-- <link href="http://netdna.bootstrapcdn.com/bootswatch/3.1.1/journal/bootstrap.min.css" rel="stylesheet"> --> <!-- For update purpuses-->
<link href="bootstrap.min.css" rel="stylesheet">

<style type="text/css">
/* Let inline verbatim have the same color as the surroundings */
code { color: inherit; background-color: transparent; }
/* Let pre tags for code blocks have the same color as the surroundings */
pre { color: inherit; background-color: transparent; }

/* Add scrollbar to dropdown menus in bootstrap navigation bar */
.dropdown-menu {
   height: auto;
   max-height: 400px;
   overflow-x: hidden;
}
</style>

</head>



<body>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  TeX: {
     equationNumbers: {  autoNumber: "none"  },
     extensions: ["AMSmath.js", "AMSsymbols.js", "autobold.js", "color.js"]
  }
});
</script>
<script type="text/javascript"
 src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<!-- newcommands.tex -->
$$
\newcommand{\Oof}[1]{\mathcal{O}(#1)}
\newcommand{\F}{\boldsymbol{F}}
\newcommand{\J}{\boldsymbol{J}}
\newcommand{\x}{\boldsymbol{x}}
\renewcommand{\c}{\boldsymbol{c}}
$$




    
<!-- Bootstrap navigation bar -->
<div class="navbar navbar-default navbar-fixed-top">
  <div class="navbar-header">
    <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-responsive-collapse">
      <span class="icon-bar"></span>
      <span class="icon-bar"></span>
      <span class="icon-bar"></span>
    </button>
    <a class="navbar-brand" href="._p4c-bootstrap-Python019.html">Numerical Methods [Real Time and Embedded Systems Programming]</a>
  </div>

  <div class="navbar-collapse collapse navbar-responsive-collapse">
    <ul class="nav navbar-nav navbar-right">
      <li class="dropdown">
        <a href="#" class="dropdown-toggle" data-toggle="dropdown">Contents <b class="caret"></b></a>
        <ul class="dropdown-menu">
     <!-- navigation toc: --> <li><a href="#5th:SolvODEs" style="font-size: 80%;"><b>Solving ordinary differential equations</b></a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:pg" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Population growth</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:pg:model" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Derivation of the model</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:pg:numerics" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Numerical solution</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:pg:prog1" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Programming the Forward Euler scheme; the special case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:pg:geom" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Understanding the Forward Euler method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:FE:gen" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Programming the Forward Euler scheme; the general case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#___sec145" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Making the population growth model more realistic</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python020.html#sec:de:growth:test:linear" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Verification: exact linear solution of the discrete equations</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#___sec147" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Spreading of diseases</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Spreading of a flu</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:FE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A Forward Euler method for the differential equation system</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:prog:spec" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Programming the numerical method; the special case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#___sec151" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Outbreak or not</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:generic" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Abstract problem and notation</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:prog:generic" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Programming the numerical method; the general case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#___sec154" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Time-restricted immunity</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:vaccine" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Incorporating vaccination</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python021.html#sec:de:flu:vaccine:discont" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Discontinuous coefficients: a vaccination campaign</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:vib" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Oscillating one-dimensional systems</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec158" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Derivation of a simple model</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec159" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Numerical solution</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:vib:special" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Programming the numerical method; the special case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec161" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A magic fix of the numerical method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:osc:Heun" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The 2nd-order Runge-Kutta method (or Heun's method)</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:osc:odesolverpy" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Software for solving ODEs</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec164" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The 4th-order Runge-Kutta method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec165" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The algorithm</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec166" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Application</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec167" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Implementation</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec168" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Derivation</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec169" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;More effects: damping, nonlinearity, and external forces</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec170" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Euler-Cromer scheme</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec171" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The 4-th order Runge-Kutta method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec172" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Illustration of linear damping</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#___sec173" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Illustration of linear damping with sinusoidal excitation</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:vib:ode2:sliding:friction" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Spring-mass system with sliding friction</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:vib:2nd" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A finite difference method; undamped, linear case</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python022.html#sec:de:vib:2nd:damped1" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A finite difference method; linear damping</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#___sec177" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Exercises</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:geom" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 44: Geometric construction of the Forward Euler method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:FE:test1" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 45: Make test functions for the Forward Euler method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:Heun:pg" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 46: Implement and evaluate Heun's method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:logistic:dtopt" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 47: Find an appropriate time step; logistic model</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:SIR:dtopt" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 48: Find an appropriate time step; SIR model</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:SIRV:padapt" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 49: Model an adaptive vaccination campaign</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:SIRV:padapt_time_limited" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 50: Make a SIRV model with time-limited effect of vaccination</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:vib:FE:func" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 51: Refactor a flat program</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:vib:ode_FE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 52: Simulate oscillations by a general ODE solver</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:vib:energy" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 53: Compute the energy in oscillations</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:pg:BE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 54: Use a Backward Euler scheme for population growth</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:pg:CN" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 55: Use a Crank-Nicolson scheme for population growth</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:fd:Taylor" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 56: Understand finite differences via Taylor series</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:vib:BE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 57: Use a Backward Euler scheme for oscillations</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#___sec192" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remarks</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:SIR:Heun" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 58: Use Heun's method for the SIR model</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:odesolverpy:decay" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 59: Use ODESolverPy to solve a simple ODE</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:osc:BE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 60: Set up a Backward Euler scheme for oscillations</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:osc:FE:general" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 61: Set up a Forward Euler scheme for nonlinear and damped oscillations</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python023.html#sec:de:exer:osc:2nd:V0ic" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 62: Discretize an initial condition</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python024.html#6th:SolvPDEs" style="font-size: 80%;"><b>Solving partial differential equations</b></a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#6th:SolvPDEs:MOLandFE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Finite difference methods</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:reduce" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reduction of a PDE to a system of ODEs</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:testproblem" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Construction of a test problem with known discrete solution</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec202" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Implementation: Forward Euler method</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:rod" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Application: heat conduction in a rod</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec204" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vectorization</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec205" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Using ODESolverPy to solve the system of ODEs</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec206" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Implicit methods</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec207" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;Exercises</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:handFE" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 63: Simulate a diffusion equation by hand</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:groundtemp" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 64: Compute temperature variations in the ground</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:compare:implicit" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 65: Compare implicit methods</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:groundtemp:adapt" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 66: Explore adaptive and implicit methods</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:CN" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 67: Investigate the \( \theta \) rule</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec213" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remarks</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:Gaussian" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 68: Compute the diffusion of a Gaussian peak</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec215" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remarks</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#2nd:exer:area:polygon2" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 69: Vectorize a function for computing the area of a polygon</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:Gaussian:symm" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 70: Explore symmetry</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec218" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remarks</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:stationary" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 71: Compute solutions as \( t\rightarrow\infty \)</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#___sec220" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remarks</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python025.html#sec:pde:diff1D:exer:stationary2" style="font-size: 80%;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exercise 72: Solve a two-point boundary value problem</a></li>
     <!-- navigation toc: --> <li><a href="._p4c-bootstrap-Python039.html#___sec267" style="font-size: 80%;"><b>References</b></a></li>

        </ul>
      </li>
    </ul>
  </div>
</div>
</div> <!-- end of navigation bar -->

<div class="container">

<p>&nbsp;</p><p>&nbsp;</p><p>&nbsp;</p> <!-- add vertical space -->

<a name="part0019"></a>
<!-- !split -->

<center><h1 id="5th:SolvODEs">Solving Ordinary Differential Equations</h1></center> <!-- chapter heading -->

<p>
<center><p><img src="figs/FE_comic_strip.png" align="bottom" width=800></p></center>

<p>
<br />
<br />

<p>
Differential equations constitute one of the most powerful mathematical
tools to understand and predict the behavior of dynamical systems in
nature, engineering, and society. A dynamical system is some system with
some state, usually expressed by a set of variables, that evolves in time.
For example, an oscillating pendulum, the spreading of a disease,
and the weather are examples of dynamical systems.
The basic laws of physics could be used, or the plain intuition, to express mathematical
rules that govern the evolution of the system in time.
These rules take the form of
<em>differential equations</em>. The reader are probably well experienced with
equations, at least equations like \( ax+b=0 \) or \( ax^2 + bx + c=0 \).
Such equations are known as <em>algebraic equations</em>, and the unknown
is a number. The unknown in a differential equation is a function,
and a differential equation will almost always involve this function
and one or more derivatives of the function.
For example, \( f'(x)=f(x) \) is a simple
differential equation (asking if there is any function \( f \) such that
it equals its derivative - the reader might remember that \( e^x \) is a
candidate).

<p>
The present chapter starts with explaining how easy it is to solve
both single (scalar) first-order ordinary differential equations and
systems of first-order differential equations by the Forward Euler
method. All the mathematical and programming details are demostrated
through two specific applications: population growth and spreading of
diseases.

<p>
Then te explanation turns to a physical application: oscillating mechanical
systems, which arise in a wide range of engineering situations. The
differential equation is now of second order, and the Forward Euler
method does not perform well. This observation motivates the need for
other solution methods, deriving then the Euler-Cromer scheme <button type="button" class="btn btn-primary btn-xs" rel="tooltip" data-placement="top" title="The term scheme is used as synonym for method or computational recipe, especially in the context of numerical methods for differential equations."><a href="#def_footnote_3" id="link_footnote_3" style="color: white">3</a></button>, 
the 2nd- and 4th-order Runge-Kutta schemes, as well as a finite difference
scheme (the latter to handle the second-order differential equation
directly without reformulating it as a first-order system). The
presentation starts with undamped free oscillations and then treats
general oscillatory systems with possibly nonlinear damping, nonlinear
spring forces, and arbitrary external excitation.  Besides developing
programs from scratch, it is also demonstrated how to access ready-made
implementations of more advanced differential equation solvers in
Python.

<p>
As progressing with advanced methods, more sophisticated and reusable programs 
are developed, and in particular, good testing strategies are incorporated, 
so that it bring solid evidence to correct computations. Consequently, 
the beginning with population growth and disease modeling examples has a very 
gentle learning curve, while that curve gets significantly steeper towards the 
end of the treatment of differential equations for oscillatory systems.

<br />
<br />
<br />
<br />
<br />
<p id="def_footnote_3"><a href="#link_footnote_3"><b>3:</b></a> The term <em>scheme</em> is used as synonym for method or
computational recipe, especially in the context of numerical
methods for differential equations.</p>


<p>
<p>
<p>
<!-- navigation buttons at the bottom of the page -->
<ul class="pager"> 
  <li class="next">
    <a href="._p4c-bootstrap-Python020.html">Next &rarr;</a>
  </li>
</ul>
<!-- ------------------- end of main content --------------- -->

</div>  <!-- end container -->
<!-- include javascript, jQuery *first* -->
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
<script src="http://netdna.bootstrapcdn.com/bootstrap/3.0.0/js/bootstrap.min.js"></script>

<!-- Bootstrap footer
<footer>
<a href="http://..."><img width="250" align=right src="http://..."></a>
</footer>
-->


</body>
</html>
    
```
