# MEAN-VARIANCE-AND-CROSS-CORELATION
## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## APPARATUS REQUIRED

•	Computer with i3 Processor
•	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results

##  Code
```
clear; clc;
function X = f(x)
    z = (2 - x).^2;
    X = x .* z;
endfunction
a = 0; b = 1;
EX = intg(a, b, f);
function Y = c(y)
    z = (3 - y).^2;
    Y = y .* z;
endfunction
EY = intg(a, b, c);
function X2 = g(x)
    z = (2 - x).^2;
    X2 = (x.^2) .* z;
endfunction
EX2 = intg(a, b, g);
function Y2 = h(y)
    z = (5 - y).^2;
    Y2 = (y.^2) .* z;
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
disp(EX, "i) Mean of X =");
disp(EY, "   Mean of Y =");
disp(vX2, "ii) Variance of X =");
disp(vY2, "   Variance of Y =");
x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```
## Output
<img width="538" height="527" alt="image" src="https://github.com/user-attachments/assets/71f1ada3-3fbd-40de-8791-774793d59119" />
<img width="765" height="599" alt="Screenshot 2025-10-28 102533" src="https://github.com/user-attachments/assets/a0c297b0-2ae0-4049-8152-7ea6365caf34" />

## TABULAR COLUMN
<img width="940" height="594" alt="image" src="https://github.com/user-attachments/assets/60b38d79-f068-4739-8fe0-2f6171361f50" />

## MANUAL CALCULATION
<img width="818" height="1454" alt="image" src="https://github.com/user-attachments/assets/4a56945b-60f3-419d-a604-cc89643a5175" />
<img width="940" height="693" alt="image" src="https://github.com/user-attachments/assets/89841c76-1b74-4a15-8317-60a1b16d70d5" />

## RESULT
hus the mean , variance and cross correlation are executed in Scilab and output is verified.
