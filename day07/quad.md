# Quad
![The screen is divided into quarters. The first shows a moving patterns of twisting coloured bars. The second is a chequerboard in 3d scrolling towards the viewer with ball sprite in an animating pattern. The third is some horizontally scrolling sine waves with a line of scrolling text in front, and the last is a spinning coloured tunnel](./quad.gif)
```
m=math
e=m.sin
p=pix
t=0
w=120
h=68
r=99
text=string.rep("Tiny Code Chirstmas ",h)
len=string.len(text)/h
function TIC()for i=0,w*h-1 do
x=i%w
y=i//w
z=y/w+.3
n=x-60
q=t/16
p(x+w,y,8+(n/z//64+y/z/16-q)%2)
p(x,y,r*e(t/h+x/w)+r*e(t/r+y/w))
u=x-w/2
v=y-h/2
dist=200/(u*u+v*v+1)^0.5
angle=q+(m.atan2(v,u)+m.pi)*2.546
if (dist>20)
then
colour=0
else
colour=angle//1+((dist+t/8)//1)%16
end
p(x+w,y+h,colour)
o=9+18*m.cos(t/80)
p(x,y+h,8+(o*e(x/16+t/40)-y)/34)
end
for i=0,128 do
ax=i*16+t/32
ay=i*64+t/64
sx=210/4
sy=88/4
px=145
py=23
x=sx+m.sin(px+ax)*sx
y=sy+m.sin(py+ay)*sy
spr(0,x+w+5,8+y,0)
end
clip(0,h,w,h)
for i=0,11 do
qq=t+48*m.cos(i*m.pi/22+t/64)
col=qq%(len*6)
chunk=len+col//6
span=string.sub(text,chunk,chunk+21)
print(span,-(col%6)-1,-1+h+i*6,14,1)
print(span,-(col%6),h+i*6,12,1)
end
clip()
t=t+1
end
```