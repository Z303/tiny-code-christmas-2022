# Day 5
![Looking straight down a red, green and blue striped tunnel rotating anti-clockwise](./day05.gif)
```
m=math
t,w,h=0,120,68
l={3,7,10}
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
t=t+1
end
```

and a formatted version

```
m=math
t,w,h=0,120,68
l={3,7,10}
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
    t=t+1
end
```