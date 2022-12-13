# Day 1
![Chirstmas trees over a sky background with a snowman to one side](./day01/day01.gif)
```
function TIC()
c,r,t=circ,rect,tri
cls(10)
f=130
h=240
w=70
r(0,f,h,6,12)
b=20
z=10
v=30
for i=40,210,70 do
r(i-z,110,b,b,4)
for j=34,94,14 do
t(i,j,i-b,j+v,i+b,j+v,6) 
end
end
for j=80,f,b do
c(150,j,z,12)
end
for q=145,155,z do
c(q,77,1,0)
end
end
```