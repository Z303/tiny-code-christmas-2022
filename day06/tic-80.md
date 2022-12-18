# Day 6
![A vertical scrolling background saying "Z303" with lines of text scrolling horizontally in a sine wave in front](./day06.gif)
```
m=math
p=print
s=string
f,h=0,68
t=s.rep("Tiny Code Chirstmas ",h)
r=s.rep("Z303",10)
l=s.len(t)/h
function TIC()cls()for i=0,24 do
p(r,0,i*6-(f%6),14)
q=f+48*m.cos(i*m.pi/22+f/64)
c=q%(l*6)
b=l+c//6
v=s.sub(t,b,b+41)
p(v,-(c%6),-12+i*6,12,1)end
f=f+1
end
```

and a formatted version

```
m=math
p=print
s=string
f,h=0,68
t=s.rep("Tiny Code Chirstmas ",h)
r=s.rep("Z303",10)
l=s.len(t)/h
function TIC()
    cls()
    for i=0,24 do
        p(r,0,i*6-(f%6),14)
        q=f+48*m.cos(i*m.pi/22+f/64)
        c=q%(l*6)
        b=l+c//6
        v=s.sub(t,b,b+41)
        p(v,-(c%6),-12+i*6,12,1)
    end
    f=f+1
end
```