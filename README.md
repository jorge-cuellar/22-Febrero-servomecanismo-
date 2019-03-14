# 22-Febrero-servomecanismo-

miFuncion1.m
function dydt=miFuncion1(t,y)
dydt = t/y;
end

miFuncion2.m
function dydt=miFuncion2(t,y)
alpha=2;
gama=2;
dydt=alpha*y-gama*y*y;
end

 miFuncion3.m
function dydt=miFuncion3(t,y)
dydt=-exp(2*y)*sin(t);
end

miFuncion4.m
function dydx=miFuncion4(x,y)
dydx=exp(x)/2*y;
end

%% l
function [t,y]=call_miFuncion1()
tspan=[0 10];
y0=1;
[t,y]=ode45(@miFuncion1, tspan, y0);
end

%% 2
function [x,y]=call_miFuncion2()
xspan=[0 10];
y0=10;
[x,y]=ode45(@miFuncion2, xspan, y0);
end

function [t,y]=call_miFuncion2()
tspan=[0 10];
y0=10;
[t,y]=ode45(@miFuncion2, tspan, y0);
end

function [t,y]=call_miFuncion3()
tspan=[0 10];
y0=0;
[t,y]=ode45(@miFuncion2, tspan, y0);
end

function [x,y]=call_miFuncion4()
xspan=[0 10];
y0=0;
[x,y]=ode45(@miFuncion4, xspan, y0);
end
