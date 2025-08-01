# Mathematica Notes : all the functions start with capital letters.
Newdocument: you code here
Mathematica has a authrotative documentation as source: Help=> wolfram documentation=> you can search any function there.
You can us it as a calculator.   
We have some quick ways: press Insert=> Typesetting=> Fraction, radical,...,RUN=Shift+Enter
 Division: N[2/3]=2./3= 0.66

No paranthese, just []: Sin[2]=>N[Sin[2]] or Sin[2.]
No output: x=5; or x:=5
check the equivalence: x==y 
Mathematic functions:Log[10,100], N[Sin[3]], Sin[2.], 1+2I, Sin[30 Degree] 
To clear old variables: ClearAll[y]                                                                                                        ,ii=I

#Algebra:
Try these functions:    (a+b)^2, Expand[(a+b)^2], Simplify[a^2 - b^2/a+b], FullSimplify[a^2 - b^2/a+b], Factor[x^2+ x^2/3], D[x^2+x,x], RandomInteger[{0, 10}], For[i = 0, i < 10, i++, print[RandomInteger[{0, 10}]]]
PlanckRadiationLaw[temperature,λ], HermitH[3,x], SphericalHarmonicY[l,m,θ,ϕ], FunctionExpand[SphericalBesselJ[3, x]]: this gives you the form of SphericalBessel func.

#Solve Equation:
1)
eq1 = 2 x + y == 3 z;
eq2 = x/y == 4 z;
eq3 = x^2 + y^2 == z^2;
Solve[{eq1, eq2, eq3}, {x, y, z}]
2)Manually placement: 
sol1 = Solve[eq1, x][[1]]
sol2 = Solve[eq2 /. sol1, y][[1]]

The smallest and biggest number mathematica can have: $MinNumber, $MaxNumber
Delta Dirak: Integrate[DiracDelta[x], {x, -1, 0}]

How to plot: Plot[x^2, {x, -10, 10}] , Plot[Integrate[ DiracDelta[a] + Dirac Delta[a - 1], {a, -10, x}], {x, -1, 5}]
Plot[1/x, {x, -10, 10}, PlotLegends -> {Salam}, PlotRange -> {-1, 2}],   

How plot many functions in one plot: Plot[{Sin[x], Sin[2 x], Sin[3 x] }, {x, 0, 2 Pi}, PlotStyle -> {Blue, Red, {Thin, Dashed, Black}}, AxesLabel -> {"x", "f(x)"}] 
#search plotstyle, we have many options there.

How plot 3D:
ListPlot[{1, 4, 6}]
 Plot3D[x^2 + y^2, {x, 1, 3}, {y, -1, 5}, AxesLabel -> {"x", "y", "z"}], 
VectorPlot[{x, 2 y}, {x, 0, 2}, {y, -1, 3}],   
VectorPlot3D[{x, -y, 3 z + x}, {x, -10, 10} , {y, -5, 5}, {z, -6, 5}] # for electromagnetic simulation
StreamPlot[{x, 2 y}, {x, 0, 2}, {y, -1, 3}, VectorPoints -> "Fine"] #current lines(field lines in electrostatic)
PolarPlot[Sqrt[x], {x, 0, 3 Pi}] ,#Polar coordinate
DensityPlot[x^2 + y^2, {x, -5, 5}, {y, -5, 5}, PlotLegends -> Automatic]
DensityPlot3D[x^2 + y^2 + z^2, {x, -5, 5}, {y, -5, 5}, {z, -5, 5} ]
Manipulate[Plot[a*x^2, {x, -5, 5}], {a, -3, 3}]

Other functions:
Asymptotic[SphericalBesselJ[5, x], x -> \[Infinity]]
Limit[Sin[x]/x, x -> 0]

Useful functions for physicists:
PauliMatrix[0],PauliMatrix[1], 

Algebra:
matrix:
A = {{1, 2}, {3, 4}};
MatrixForm[A]# you ccan see matrix
MatrixForm[Transpose[A]]#Transpose the matrix
Det[A]
Inverse[A]
Eigenvalues[A]
Eigenvectors[A]

b = PauliMatrix[1]
c = PauliMatrix[2]
Dot[b, c]

Dot[{1, 1}, {2, 3}]

Needs["VectorAnalysis`"]
SetCoordinates[Cartesian[x, y, z]]

e = {x, y, x}
Div[e, Cartesian]

Curl[e, Cartesian]

b = {1, 2, 3};
c = {4, 5, 6};
Cross[b, c]

Norm[{-3,6,-2}]

Grad[x^2 + y^2 + z^2, Cartesian[x, y, x]]
Laplacian[x^2 + y^2 + z^2, Cartesian[x, y, x]]

Reduce[x^2 + x < 0, x]
Taylor expansion:
Series[Exp[x], {x, 0, 5}]

How solve differtial equations:

eq4 = y''[x] == y[x];
DSolve[{eq4, y[0] == 1, y'[0] == 1}, y[x], x]

eq4 = y'[x] == x;
DSolve[eq4, y[x], x]

Numerical Solving:
NDSolve -> check it !




