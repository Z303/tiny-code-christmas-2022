# Day 4
![Colour lines making shifting patterns and forming shapes](./plasma.gif)
```
f=0
w=240
s=45
t=29
a=121
b=235
o1=189
o2=112
o3=45
o4=15
m=math.cos
function TIC()
for i=0,w*136 do
x=i%w
y=i//w
n=x+(f/4)
o=x+(f/10)
px=a+a*m(o1+n/a)+b+b*m(o2+o/b)
p=y+(f/3)
q=y+(f/50)
py=s+s*m(o3+p/s)+t+t*m(o4+q/t)
pix(x,y,i+py+px)
end
f=f+3
end
```
