# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen<br>
clear all; % clear screen<br>
close all; % close all figure windows<br>
wc1=input('enter the value of cut off frequency wc1'); <br>
wc2=input('enter the value of cut off frequency wc2'); <br>
N=input('enter the value of filter'); <br>
alpha=(N-1)/2; <br>
eps=0.001; <br>
%Band Pass Filter Coefficient<br>
n=0:1:N-1; <br>
hd=(sin(wc1*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)<br>
%Bartlett Window Sequence <br>
n=0:1:N-1; <br>
wh = 1 - abs(n - alpha) / alpha;
hn=hd.*wh<br>
% Plot the Band Pass Filter with Hanning Window Technique<br>
w=0:0.01:pi; <br>
h=freqz(hn,1,w);<br>
plot(w/pi,abs(h),'blue');<br>


## OUTPUT:
![WhatsApp Image 2025-11-23 at 16 05 54_02d55214](https://github.com/user-attachments/assets/3903df33-18ff-42b7-8b72-9efff1cd1672)


## RESULT:
![WhatsApp Image 2025-11-28 at 22 30 16_8e4d1494](https://github.com/user-attachments/assets/0d2baa58-9e83-41d0-9be6-65ae1b197497)
