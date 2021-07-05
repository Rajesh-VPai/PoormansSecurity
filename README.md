# Random Number 
#.	INTRODUCTION
The Random Number Java Program is a Differential PRNG(pseudorandom number generator). It uses the simple ODE(ordinary differential equation )F(x)==F’(x) for finding the new Random Number State (Xn+1) from the old or initial state (Xn). At the high level , it uses the equation:
Xn_LCG = (Xn_LCG + ConfuseValue + DiffusionValue - SupportValue + SurprisalValue) % (Modulus);

At the low level it uses the entropy equation povided along with the seed entropy variables a,b,c,d to generate the new state Xn+1.
Xnplus1 = (long) ((LCGexpValue2.eval() + x) % (Modulus ));
where LCGexpValue2.eval() is F’(x) value

#. Packages
a)	Calculus :Expression Lambda, Differentiation Lambda, Integration Lambda, etc.
b)	TestHarness: Test Suite for Calculus (including Regression Tests with Answers)
c)	DOETest : Automated Test Suite for RandomNumber ( using Taguchi Design of Expriments and associated Config Files in data\DOESelfTestConfig )
d)	RandomNumber:Code for 2 RNGs:
i.	UserResearchStudy
ii.	RNGDiff
e)	Plot: Pixel Plotter for RNGDiff based on javax.swing

#High Level Design:
 The purpose of the Java DPRNG is :
1.	To address the Industry needs of a Random Number Generator as there are few Java Random Number Generators available on the Internet.
2.	To help the University Freshman in Advanced College Courses get answers to simple design decisions through the Study Functions :
a.	//StudyRandomValues(i); : Sample code for comparision of mathematical operations (+,-, *, /) on 2 different Random Values in a Series
b.	//StudyLogicValues(i); : Sample code for comparision of 2 Random Values in a Series (usage of >, < , == operators with 2 different random values) as well as comparing 1 random variable with a constant(64)
c.	//StudyXORLogicValues(i); : Sample code for XOR Logic of 2 Random Values in a Series (usage of p=> q i.e p implies q)
d.	//StudyRandomLinearEqns(i); : Sample code for 2 Random Values in a linear equations and Constants
e.	//StudyRandomSecurity(i); : Sample code for 2 Random Values in Encryption and Decryption)
f.	Xn_Series4:y=mx+c where all m, x, ‘+’ and c are randomly varied and to study if this can be guessed in the Xn_Series4 Series Object
3.	To demonstrate the power of Java Calculus through and real life application


#Forming the Project Folder:
i.	Create data directory
1)	Create DOESelfTestConfig with the files:
a.	DOEConfig000  :No Extension
b.	DOEConfigDefault:No Extension
c.	DOESelfTestConfig:No Extension
ii.	Create logs directory.
	n src Folder:
1)	Create Calculus Package with below files (10 files)
a.	ConsoleColors.java
b.	DiffrIntegrSep.java
c.	FuncInvSep.java
d.	MathematicalTestHarness.java
e.	MathsContxtLAv.java
f.	RNGDiff.java
g.	SimpleAlgebraSep.java
h.	SubsStrSep.java
i.	TestHarness.java
j.	Usage.java
2)	Create RandomNumber Package with below files (9 files)
a.	Rand_Pool.java
b.	RandomFactorialLCGDyDx.java
c.	RandomNumber.java
d.	RandomSeries.java
e.	RandomSimpleLCG.java
f.	RNGDiff.java
g.	SSCCE.java
h.	UserResearchStudy.java
i.	XORRandom.java
3)	Create DOETest Package with below files (3 files)
a.	HDOEDefine.java
b.	TestHarnessDOE.java
c.	UsageDOE.java
4)	Create Plot Package with below files (2 files)
a.	Screen.java
b.	SSCCE.java
5)	Create TestHarness Package with below files (12 files)
a.	TestHarnessAlgebra.java
b.	TestHarnessCoefficients.java
c.	TestHarnessExpression.java
d.	TestHarnessFInverse.java
e.	TestHarnessIndConstant.java
f.	TestHarnessInfinityNaN.java
g.	TestHarnessIsolation.java
h.	TestHarnessNames.java
i.	TestHarnessParentheses.java
j.	TestHarnessPredicate.java
k.	TestHarnessSignedX.java
l.	TestHarnessUnitTest.java
6)	Add log4j.properties to src file

#RUNNING THE PROGRAMS
Using Netbeans 8.2, 
1)	Open UserResearchStudy.java. 
2)	Right Click
3)	Select Run File
