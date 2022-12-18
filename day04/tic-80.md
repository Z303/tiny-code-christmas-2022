# Day 4
![Coloured line distorting in various shapes](./day04.gif)
```
s=math.sin
t,w,h,r=0,240,136,99
function TIC()for i=0,w*h do 
x,y=i%w,i//w
u=r*s(t/h+x/w)v=r*s(t/r+y/w)pix(x,y,u+v)end t=t+1 end
```

and a formatted version

```
s=math.sin
t,w,h,r=0,240,136,99
function TIC()
    for i=0,w*h do 
        x,y=i%w,i//w
        u=r*s(t/h+x/w)
        v=r*s(t/r+y/w)
        pix(x,y,u+v)
    end 
    t=t+1
end
```