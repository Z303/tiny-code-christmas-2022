# Day 2
![Amountain range with snow falling in front](./day02.gif)
```
t=0
function TIC()
h=136
f=h-6
w=240
m=70
cls(10)
rect(0,f,w,6,12)
for i=20,650,160 do
x=i&w
tri(x,90,x+m,f,x-m,f,13+i/w)
end
for i=0,h*3 do
j=i/h
s=(i*23)%w
y=(i+t*j/5)%h
x=s+5*math.cos(j*64+s+y/10)
circ(x%w,y%h,j%2,12)
end
t=t+1
end
```