# Day 11
![A spinning cube made from spheres rotating with a grey background with a sliding division](./day11.gif)
```
v=math.sin t=0TIC=load"s={}for d=-25,25,6 do for w=-25,25,6 do for n=-25,25,6 do f=v(t)o=v(t-11)q=d*o-f*w r=d*f+o*w b=n*o+f*r s[1+#s]={x=q*o-f*b,y=r*o-f*n,z=q*f+o*b+400}end end end table.sort(s,function(u,a)return a.z<u.z end)u=v(120*t/68)*124 cls(15)rect(120+u,0,600,600,14)for c=1,#s do for e=0,2 do circ(120+600*s[c].x/s[c].z-e/2,68+600*s[c].y/s[c].z-e/2,3-e,s[c].x<u and e+8or e)end end t=.01+t"
```

and with some formatting

```
sin=math.sin

angle=0

function TIC() 
 pts = {}
 for x=-25,25,6 do
 for y=-25,25,6 do
 for z=-25,25,6 do
 	s=sin(angle)
 	c=sin(angle-11)

 	px= x*c - y*s
 	py= x*s + y*c

 	qy= py*s + z*c

		pts[#pts+1]=
		    {x= px*c - qy*s,
		     y= py*c - z*s,
		     z= px*s + qy*c + 400}
	end
	end	
 end

 table.sort(pts,function (a, b) 
			return a.z>b.z end)

	a=124*sin(angle*120/68)

	cls(15)
	rect(120+a, 0, 600, 600, 14)

	for p=1,#pts do 				 		
		for w=0,2 do 
			circ(pts[p].x*600/pts[p].z+120-w/2,
			     pts[p].y*600/pts[p].z+68-w/2,
			     3-w, pts[p].x<a and 8+w or w)
		end 
	end
	
 angle=angle+.01	 
end
```
