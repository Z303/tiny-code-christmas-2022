# Scroller
![Looking straight down a red, green and blue striped tunnel rotating anti-clockwise with scrolling lines of text flowing in a sine wave](./scroller.gif)
```
m=math
z=print
t,w,h=0,120,68
l={3,7,10}
text="Hello. I'd forgotten how much I hate writing scrollers. Wrap. "
scrolltext=string.rep(text,3)
len=string.len(scrolltext)/3
function TIC()
for y=-h,h do 
for x=-w,w do 
a=t/16+(m.atan2(y,x)+m.pi)*2.546
d=999/(x*x+y*y+1)^0.5
q=l[1+(a*12//16)%3]
if (d>h)
then
c=0
else
c=(q~((d+t/4)//1)%3)
end
pix(w+x,h+y,c)
end
end
for i=0,22 do
temp=t+48*m.cos(i*m.pi/22+t/64)
pos=temp%(len*6)
start=len+pos//6
fine=pos%6
visible=string.sub(scrolltext,start,start+41)
z(visible,0-fine-1,-1+i*6,15,1)
z(visible,0-fine,i*6,12,1)
end
rect(212,126,27,9,0)
rect(225,127,13,7,12)
z("Z3",214,128,12)
z("03",226,128,0)
t=t+1
end
```