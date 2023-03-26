# breathing-rate
dataset = dlmread('Normal_Breathing.txt', '\t', 2, 0); 
s = dataset(:,1);
%y = dataset(:,2)
data = s;
N1 = length(s);
t=0:1/500 : N1/500-1/500;
plot(t,s)
title('Plot of signal')
xlabel('Time')
ylabel('Sample(s)')
[pks,locs,w,p] = findpeaks(data);
a=size(pks);
peak_count = (a/2);
