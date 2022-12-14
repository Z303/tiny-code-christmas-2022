# Day 2
![A chequerboard in shades of blue scroling up with a white Z£03 text in the centre](./day02.gif)
```
t=0
s=10
r=32
w=240
m=math
function TIC()
a=t/r
p=m.sin(a)*r
q=m.cos(a)*r
for i=0,w*136 do
x=i%w
y=i//w
u=(p+x)//s
v=(q+y)//s
c=(u+v)%2
pix(x,y,8+c)
end
print("Z303",108,64,12)
t=t+1
end
```