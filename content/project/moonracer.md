---
title: moonracer
date: 2023-09-26
tags:
  - haskell
  - game
---

A tiny game.

Source: https://github.com/TristanCacqueray/moonracer

```haskell
#!/usr/bin/env -S stack script --compile --resolver lts-20.13 --package gloss
import Imports;a=(b,b,b,[(m(p`mod`70-35),m(5+p`mod`50))|p<-[0,88..]]);b=(0,0)
main=play(InWindow"MoonRacer"(800,600)(5,5))white 30("",b,a)g i l;d p=scale p p
c(p,q)=translate(p*10)(q*10);e p=c p(Circle 3);f p q=c p(d 10$line[b,q])
h(EventKey(SpecialKey p)q _ _)=(p,bool 1 0$q==Up);h _=(KeyF1,0);j=(*)0.8;o=True
g(p,_,(_,q,_,r:_))=c(0,-29.7)(d 0.1(Text p)<>e q<>e r);i p(q,(r,s),t)=let
 (u,v)=h p;w|u==KeyRight=v|u==KeyLeft=n v|o=r;x|u==KeyUp=v|o=s in (q,(w,x),t)
k=0.3;n=negate;m=fromIntegral;l p(q,r@(s,t),((u,v),(w,x),(y,z),α@((β,γ):δ)))=let
 ε μ ν=abs(μ-ν)<1;(ζ,η)|ε w β&&ε x γ=(u+1,δ)|o=(u,α);θ=(w+(y+s)*k,x+(z+t)*k)
 ι=(j(s+y),j(t+z-k));κ=((ζ,v+p),θ,ι,η);λ|u>9=(show v,b,a)|o=(q,r,κ)in λ
-- ^10 ------------------------------------------------------------------ 80> --
```
