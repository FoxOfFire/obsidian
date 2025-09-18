# Logika 12

Prenexre hozás szabályai:
!*A*xP(x) => *E*x(!P(x))
!*E*xP(x) => *A*x(!P(x))

*A*xP(x)^*A*xQ(x,x) => *A*x(P(x)^Q(x,x))
*E*xP(x)v*E*xQ(x,x) => *E*x(P(x)vQ(x,x))
*A*xP(x) (^/v) *A*y*E*zQ(y,z) => *A*x( P(x)(^/v)*A*y*E*zQ(y,z) )
*A*xP(x) (^/v) *E*zQ(z,z) => *A*x*E*z( P(x)(^/v)Q(z,z) )

______________________________________________________________________

Skollemre hozás szabályai
*E*xP(x) => P(*a*)
*A*x*E*yQ(x,y) => *A*xQ(x,f(x))
*A*x*E*y*A*z(Q(x,y),P(z)) => *A*x*A*z(P(x)^Q(f(x),z))
*A*x*E*y*E*z(P(x)^Q(y,z)) => *A*x(Q(x,f(x))^P(g(x)))
*A*x*A*y*E*z(P(x)^Q(y,z)) => *A*x*A*y(P(x)^Q(y,f(x,y)))

______________________________________________________________________

*E*x(*A*z*A*y(!Q(y) > !P(z,x)) ^ *A*yP(x,y)) |= *E*xQ(x) ^ *E*xP(x,x)

1. Ex(AzAy(!Q(y) > !P(z,x)) ^ AyP(x,y)) (> átírás)
1. Ex(AzAy(!!Q(y) v !P(z,x)) ^ AyP(x,y))
1. Ex(AzAw(Ay(!!Q(y) v !P(z,x)) ^ P(x,w)))
1. ExAzAwAy((!!Q(y) v !P(z,x)) ^ P(x,w))
1. AzAwAy((!!Q(y) v !P(z,*a*)) ^ P(*a*,w))
1. AzAy(Q(y) v !P(z,*a*)) ^ AwP(*a*,w)

S = Q(y)v!P(z,*a*) , P(*a*,w)

!(*E*xQ(x) ^ *E*xP(x,x))
*A*x!Q(x) v *A*xP!(x,x)
*A*x*A*y(!Q(x)v!P(q,q))

S = Q(y)v!P(z,*a*) , P(*a*,w), !Q(x)v!P(q,q)

1. Q(y)v!P(z,*a*) \[*e*S\]
1. P(*a*,w) \[*e*S\]
1. !Q(x)v!P(q,q) \[*e*S\]
1. Q(y) \[res(1,2)\](z||*a*,w||*a*)
1. !P(q,q) \[res(3,4)\](x||y)
1. [] \[res(2,5)\](q||*a*,w||*a*)

______________________________________________________________________

!Ex(EyP(x,y) > AyEz(!Q(y,z))) |= ExEy(P(x,y)^Q(x,y))

1. !Ex(EyP(x,y) > AyEz(!Q(y,z))) (>)

1. !Ex(!EyP(x,y) v AyEz(!Q(y,z))) (!->)

1. Ax(!(!EyP(x,y) v AyEz(!Q(y,z)))) (!->)

1. Ax(!!EyP(x,y) ^ !AyEz(!Q(y,z))) (!! !->)

1. Ax(EyP(x,y) ^ Ey!Ez(!Q(y,z))) (!->)

1. Ax(EyP(x,y) ^ EyAz(!!Q(y,z))) (!!)

1. Ax(EyP(x,y) ^ EyAz(Q(y,z))) (AA\<-)

1. Ax(EyEw( P(x,y) ^ Az(Q(w,z)) )) (A\<-)

1. AxEyEwAz( P(x,y)^Q(w,z) ) (f(x) g(x))

1. AxAz( P(x,f(x))^Q(g(x),z) ) (\<-^->)

1. AxP(x,fx) ^ AyAz(Q(g(y),z))

1. !ExEy(P(x,y)^Q(x,y)) (!->)

1. Ax!Ex(P(x,y)^Q(x,y)) (!->)

1. AxAy( !(P(x,y)^Q(x,y)) ) (!->)

1. AxAy( !P(x,y)v!Q(x,y) )

S = P(x,f(x)), Q(g(y),z), !P(x,y)v!Q(x,y)

1. P(x,f(x)) \[*e*S\]
1. Q(g(y),z) \[*e*S\]
1. !P(x,y)v!Q(x,y)\[*e*S\]
1. !Q(x,f(x)) \[res(1,3)\](y||f(x))
1. \<> \[res(2,4)\](x||g(y),z||f(g(y)))

______________________________________________________________________

K = {P(x,z)v!Q(f(x),g(z)), !P(g(y),u)vR(f(u)), !S(t), !R(s), S(*b*)vP(w,*b*)vQ(v,w)}

1. !S(t) \[*e*K\]
1. S(*b*)vP(w,*b*)vQ(v,w) \[*e*K\]
1. P(w,*b*)vQ(v,w) \[res(1,2)\](t||*b*)
1. !P(g(y),u)vR(f(u)) \[*e*K\]
1. Q(v,g(y))vR(f(*b*)) \[res(3,4)\](w||g(y),u||*b*)
1. !R(s) \[*e*K\]
1. Q(v,g(y)) \[res(5,6)\](s||*b*)
1. P(x,z)v!Q(f(x),g(z)) \[*e*K\]
1. P(x,z) \[res(7,8)\](v||f(x),y||z)
1. !P(g(y),u)vR(f(u)) \[*e*K\]
1. R(f(u)) \[res(9,10)\](x||g(y),z||u)
1. !R(s) \[*e*K\]
1. [] \[res(11,12)\](s||f(u))

round 2

1. P(x,z)v!Q(f(x),g(z)) \[*e*K\]
1. S(*b*)vP(w,*b*)vQ(v,w) \[*e*K\]
1. S(*b*)vP(g(z),*b*)vP(x,z) \[res(1,2)\](v||f(x),w||g(z))
   3f. S(*b*)vP(g(*b*),*b*) (x||g(z),z||*b*)
1. !P(g(y),u)vR(f(u)) \[*e*K\]
1. S(*b*)vR(f(*b*)) \[res(3f,4)\](y||*b*,u||*b*)
1. !S(t) \[*e*K\]
1. R(f(*b*)) \[res(5,6)\](t||*b*)
1. !R(s) \[*e*K\]
1. [] \[res(7,8)\](s||f(*b*))
