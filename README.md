# PracticaMatlab3
Tarea
clear
nneg=-10:-1; %variables negativas
npos=1:10;   %variables positivas
Fnneg=(1./(j*nneg*pi)).*(-3*exp(-j*nneg*6*pi/7)+2*exp(j*nneg*2*pi/7)+exp(-j*nneg*12*pi/7));
%funcion exponencial de las series de fourier de numeros negativos
Fnpos=(1./(j*npos*pi)).*(-3*exp(-j*npos*6*pi/7)+2*exp(j*npos*2*pi/7)+exp(-j*npos*12*pi/7));
%funcion exponencial de las series de fourier de numeros positivos
F0=10/7; %funcion final
n=[nneg, 0, npos]; %variable contenedora de numeros
Fn=[Fnneg, F0, Fnpos]; %variable contenedora funciones
stem(n*(1/7),abs(Fn)) %funcio abs saca el valor absoluto de los elementos
grid on 

