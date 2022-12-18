# Intro
![A chequerboard in shades of blue scroling in a circle and zooming in and out with a white Z303 text in the centre and some ball sprites in a pattern](./sprites.gif)
```
t=0
l=10
h=80
w=240
m=math
r=128
function TIC()
a=t/r
p=m.sin(a)*r
q=m.cos(a)*r
j=(h-l)/2
s=l+j+m.cos(t/h)*j
for i=0,w*136 do
x=i%w
y=i//w
u=(p+x)//s
v=q+y
pix(x,y,8+(u+v/s)%2)
end
print("Z303",108,14,12)
for i=0,256 do
ax=i*16+t/32
ay=i*32+t/64
sx=232/2
sy=88/2
px=145
py=23
x=sx+m.sin(px+ax)*sx
y=sy+m.sin(py+ay)*sy
spr(0,x,32+y,0)
end
t=t+1
end
```

and a formatted version

```
t=0
l=10
h=80
w=240
m=math
r=128
function TIC()
    a=t/r
    p=m.sin(a)*r
    q=m.cos(a)*r
    j=(h-l)/2
    s=l+j+m.cos(t/h)*j
    for i=0,w*136 do
        x=i%w
        y=i//w
        u=(p+x)//s
        v=q+y
        pix(x,y,8+(u+v/s)%2)
    end
    print("Z303",108,14,12)
    for i=0,256 do
        ax=i*16+t/32
        ay=i*32+t/64
        sx=232/2
        sy=88/2
        px=145
        py=23
        x=sx+m.sin(px+ax)*sx
        y=sy+m.sin(py+ay)*sy
        spr(0,x,32+y,0)
    end
    t=t+1
end
```