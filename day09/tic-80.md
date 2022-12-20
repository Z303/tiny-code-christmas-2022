# Day 9
![Colour circle leaving trails spinnig around on screen. Filling the screen with different colours as they pas over the iamge](./day09.gif)
```
m=math
s=m.sin
t=0
cls()
function TIC()for i=0,578 do
j=i%47poke(16320+j,s(j)^2*255)
x=i%17-8
y=i//17%17-8
a=i//289*m.pi
u=120+s(a+3.12*t-11)*110
v=68+s(a+2.54*t)*60
if (x*x+y*y<64) then
q=pix(u+x,v+y)pix(u+x,v+y,1+q)end
end
t=t+.05
end
```

and with some formatting

```
m=math
s=m.sin
t=0
cls()
function TIC()
for i=0,578 do
    j=i%47
    poke(16320+j,s(j)^2*255)
    x=i%17-8
    y=i//17%17-8
    a=i//289*m.pi
    u=120+s(a+3.12*t-11)*110
    v=68+s(a+2.54*t)*60
    if (x*x+y*y<64) then
        q=pix(u+x,v+y)
        pix(u+x,v+y,1+q)
    end
end
t=t+.05
end
```