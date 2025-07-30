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

