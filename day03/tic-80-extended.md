# Day 2
![A chequerboard in shades of blue scroling ina circle with a white Z£03 text in the centre](./day03extended.gif)
```
t=0
s=10
w=240
m=math
r=32
function TIC()
a=t/r
p=m.sin(a)*r
q=m.cos(a)*r
for i=0,w*136 do
x=i%w
y=i//w
u=(p+x)//s
v=q+y
pix(x,y,8+(u+v/s)%2)
end
print("Z303",108,64,12)
t=t+1
end
```

