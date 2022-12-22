# Day 10
![Four cycling screens. A spinning colour wheel. A chequerboard in 3D. A morphing colour shapes. A vertical sine wave](./day10.gif)
```
m=0 a=240j=136s=99TIC=load"b=m%(a*4)d=b%a e=b//a for t=0,j*a do c=t%a g=t//a p={c>d and 0or 1,g<d and 2or 1,a-c>d and 2or 3,j-g<d and 0or 3}n=p[e+1]i=c-a/2q=g-j/2r=.3+g/a f=c-a/2if n==0then k=2.546*(math.atan2(q,i)+math.pi)+m/16 elseif n==1then k=8+(f/r//64+g/r/16-m/16)%2 elseif n==2then k=s*math.sin(m/s+g/a)+s*math.sin(m/j+c/a)else k=14+(math.sin((m+g)/16)*16-c-32)/100%2 end pix(c,g,k)end m=m+1"
```

and with some formatting

```
tick=0
width=240
height=136
r=99
function TIC()
	frame = tick%(width*4)
	fade = frame%width
	part = frame//width

	for i=0,width*height do
		x=i%width
		y=i//width

		whicheffect={x>fade and 0 or 1,
					 y<fade and 2 or 1,
			   width-x>fade and 2 or 3,
			  height-y<fade and 0 or 3}
		
		effect=whicheffect[1+part]

		u=x-width/2
		v=y-height/2
		z=y/width+.3
		n=x-width/2

		if effect==0 then 
			colour=tick/16+(math.atan2(v,u)+math.pi)*2.546
		elseif effect==1 then
			colour=8+((n/z//64+y/z/16-tick/16)%2)
		elseif effect==2 then
			colour=r*math.sin(tick/height+x/width)+r*math.sin(tick/r+y/width)		
		else
			colour=14+((16*math.sin((y+tick)/16)-32-x)/100)%2			
		end
		
		pix(x,y,colour)	
	end
	tick=tick+1
end
```
