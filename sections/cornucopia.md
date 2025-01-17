# Chapter 7: Cornucopia

You have entered the seventh dungeon. You stand at the bottom of the staircase where you entered, facing east. A gnome sits on the bottom stair, sipping from a flask of mushroom brew. As he looks up at you, then down at the purse of stacking on your belt, you recognize him as the cartographer from the first dungeon. He leans forward, as if about to speak. With a magic marker and a flick of the wrist, he scribbles a line of credit onto your purse, in the shape of register S. He pauses for a moment, then sits back, taking another sip.

The stack is only a window into the bottom of a towering column of slots, indexed from zero. Above the stack, the top of the column remains hidden. As the stack grows or shrinks, more or less of the column is revealed, without any slots in the column being added, moved, or removed. Whether hidden or revealed, each slot retains any number written to it. All slots are initially zero.

Register S serves as both stack size and stack pointer. It always points to the slot just above the top of the stack. Initially, register S points to the bottom slot, indicating an empty stack. Pushing writes a number to slot S, then increments S. Popping decrements S, then reads a number from slot S. Nevertheless, both pushing and popping work as before in practice.

With plenty of challenges ahead, you consult the map:

```
{=#}({]}(##}#]{}(#)R##](][)]}{=4cO2=}Rc5=#R{((((]{#}{)}}]{(=)[(#R]{([{{#]}([(]
)lXT9}#D#}qs:VE0gE>h3ZzUw(TW3k2{ewzF,%8.r9K9dm{4sR93uX1BVi{(8uL1#rhq*=k{Il*O*(
#I)Kt###q#wv*zEs;{3e###K04Kg0>U#}n[W.o)]X]3wtQ}>tLJ71QXwn;t7Y/A(#zcaANV)[Jc%T}
]Gmfaj###.}(}A+U5IjW##McHFOsy}N#Y]%Fv{U5I}#D7Ri>T5oRX{aM1{[#DbY#}S#DD>BtQ(MBd[
{A1Rh3EnYQes={dzRw7M8/n0CUqfmSjXN5hlIM>C3TVlIX9*,6JC.3BLGN%bbCEd2hy,/ZIhqgT3.(
]fX]osz-##}3c(Xmq]eW:]YNK8VRzEu;h://J5g3bQ=#d9(9hB0;W,m#J6J#rlqJ.mQ+[M:#TF#Dh]
0A3(i#zuG#W)4>.B.Z}4}y1eAv;).)gs0co/F:C(yC2Z;99{GtZ#-.},{78xr8+o0Y%mSfT=#fL]9=
NNZhj#<rKyI9TdIxayT((WV7#R#{f=A]n,+hhA6gVA/426W):Lob#iy#07r]fu#qHqq[O)6csN#rm=
u:c=4s9;21a]}RLCiU{f)9F;Y[q.RrgtXZ#Q;Mnro#*jU+{RyOMUTAzqAOXa.tUy+iw5,v%xd*[eQN
iHU%C3##)GnCxM+TzIVd9BsojVZrIUN*uI:yRWaUd%Dyt29]]nORMR,HtUq}Drhm]#1[Ye(5#Z}h/]
c:aC6[H7d)tc)FX.iko>hm9q}e(oD]0,iiM/ICtRyLVlY1aSArDOSWumd+ugElR-qjM0Y[T>Ghi}l)
KU[u]{m%RM5z89>aG.h[A2(tZRjoT]]Rc](dV[N}-0ZsT1(0-/4+(Go}s8Bv8uvkanE.LEg(}Y(GXR
Rm}V{rR>I4HA1xZZH*()zU,9qWzXmwXT{,V*WKBxzJlmOWDKm7{(Ro1KKJQy0WNm4n.7}EAYtUR8-#
)c]Egdk4Ue;.rgs{z)77Y>HKkQLOVcH[tkR2)#-kY,I{1N#YCL#bLAWb1sY:Wq1}2=I#0*=nbRt;==
#]}{Q{I,(Rn5},JR8Ro;*7A:SQSGSJ>Nu}c4BbY,mMUR>>OLdqEr,40[mh,Zodm-AOLGlS*Ud5V6:{
]YM7%wIi=AZ.In0Wl)RG/DMRYA6cx(icIB#i1z3>cKOeXQg>#aXyF.{{]nwvCe55Qyw;E>,wl.#6s)
[RVBl=;>svGal5GyyDlA[MTh-}%E]azAO}]x4=yNE3e3(Oq{}oU5w;9VJBIdWx2Iv7aYR2#WCQq#Q{
]4>(969ygIzgLByrDou[ee}qI(Q9=1[[0N3cW,osh[t)icR>[zCZlycWR[S>cn]AR{](fmw(CJ#hU)
}9Ij#3[cK}s.Jh3bD)3U}a))hJ{fU#XQ0GA=U6XM5wiHOOxIhNfz-KJ*OL4v=sB/b).MzYWRGRc>:[
=ueInxn(fN).Zd]QlcxbTB6TzoIT{](qD}N%rwl[a>Xq5-8ReUIjo}lIfsN-U=jy#w)#+[0mm%Fn7[
#H)IsV[(B,j.5St)-O,[Dq[TcY297tlvkt/2(QOd,Gs#{wUT=}]f#{+U*89MX5Tk5{zt)DDJm6YRA)
{n7##LQCjf})u1=1jK8X[m}HgK}8o)s{]vt.mZIwWEW}#]NZNr[xe#9g{Yd.2n(Qf#cn)%#=bh==J[
}==wbHykFmR4-2ymNiee1G+FSOrDj4RaK7SMsynn0HqbEyWU5kFC:,rmiya0YXK+8nDlGk2qj-J:GR
#c8EiR[#OeJ4mwA])[#M{a(t:SALf71cn#]s[R5=]iQgqF(wulN(g(S#NOEA}}Z#2#[9])OWhnRS7S
#Ru(*Ykyqz/nfLgm8}z.9{T5#4;1wIm(Ivg9%sTO-UQ)aYmJC)k0LnhWh/Wu3+rTD5;87a:hLxN3r:
#[){({]#{}{#[{}RF%w>])#{{({}{#RR[)*2RR)})#}[#(R[(}#{))=#Rr(=}]]##(=FHI(}{](]}]

##[()#)}R#R[#){[)}{R)[}#[(](]}(](=#[}RaEf7kMJ/kj4C)RUI}###=])[##{#[#=)[[R#){=}
]{Yf8)Rj[CQCKt-x68<nJ6ZiIVlcHo}L:BwG*/dH={##(}#[Ec3ofu(Wzn5IGi%E)R#(;cER+.0Hu]
rJ8Zh+a>v{[[]4)W#ENOWb=Xyh>LV<VORxoIRS>;/>BTEt%<rKs).l{]mB[x:(MG4W7}>E1V3cmIj(
-=xVRc[CcGNav73{aR51>IG*#D)R:NU=D+h}#n5#l#-n[X9<W)m=][4Lg##rUagG(Y[E4<[KTFY(8}
a{V6F]}H#Mqcl)Cc]g2nAtZCJq[>1YvTQ7>#1U<OHW>)snrtrZx]d-:8YLQhuM81%I:2=ufcFI>},(
=hqv,7V2liVa#dR1)6t[Nk1763M2scBxDXa]OYg#E#YD.xY{Q,}rCSTARuU{,S{CI).it#Y}0SS9n)
[F+#qQW3)*#hc<i=dNNh+c%(U7%QRWGZ2}N8nXr6}={1yb>K)c*5FQtV3(>KLaL,8EU*a}Xz3I6LR{
}XmfL>d2tx]>Y%Rm--=fafEc%En.(Xt*5Fxx0ONm6A*R6x>2x,FH>7.uD]h>2d2w-1HBVTZ(3)73A[
([]{y};llB+%u26>2{{#C-xqsU.=.6yV[x1QmciYL9}C}NW#ja]oG22/f:Hfhw6tMuGgCZ=wYB93f{
[kqH#2EsEdD>hh/MOTQIQ:UR3[:U-M]T41Az)S7rz=7m,>db+=-gMMTZg[CRHN]cYOV1)GD(aa,of)
#j)7Myrt=,J%#ut0Cgv<y{}[DvRvQ2]*IE9LnUBwnyB4s6sSuTeH)hsT#%d(dewHYm>dJg#<.smlS)
RaEO))GT#VE3}f<YrXa0j7),iAaBNbrd8Eox}(w6+W]M*QyJyoz6R4KaDimATUe-u:#+,#}ZG(x(qR
#G#eSn8<[,.ZanuYCU+RWkWEe3N1Lf3r#OYZFXmlJlJ##5#yO0=}aWYZER%)91J]K8;v#a{]A1Tti#
#t[Eg72[#u--1%GrARBTC<]2DNz/eJ)w)0SX(+rR1j9gl-4;z9xXWz1AN>swb9Xa:SATu.LezFVyR=
{fHe-zVS-47N096kl-n%kFTYBLGjTj<Wwum-O{8)x>#0<<#]9dRv-v[{O%BwjW8-xv;]{5)v+7KRx3
(ySKm)Xoe38a0+lroear66:mwu%)#r%h#I7[i3n<7{RE0h]<DCdLUCzA8ZmNZ3/h>>1Og</m)#Eq)}
{.-Wi>n<x,e(I#CZ=>%t1G{r{YxW7w0gtUWl={sT#n8]C=bgcr(OBn##isyo/-mG1O,N8f[b}=9Br(
]t<H:R=*uiCQjL>ZKyiArlk#(t=2sh:v2m=nK+]N];=xIVl<:W*{r[I4[F,<ENyY5n(f=+q2=YD}q>
[dR>I4h7KK])V]mn%MtiuyvwOzw{uvIauBnBmZA983zI2CVIr1IzE},XXgG)H08:wZEynj9;{1C<D=
(s2:Yxla.UB2=#[9Xf2#E}SK}B{F6TWC[+TvJL(7#<I#4i3#nV#K32#=fzMfLd2ai:=qsu}%t}ax)#
[M6j%wIgeJ>,ngM[Q*q>{#d#eB=#qC}IV,9g{iUz#M;#CcG=8s:)Q}>zdb)jVyBmWv>(N#}w2ga1y)
#O=1Z7x;%Q}:[H#3NXQ(UcrEtv},gT}mndh->LNHv;ey%Tx;azr1c45gdTA1mNm;34msU[Re[HVA(}
[M=.T#Scj[nER}iogTtzG7G#k=u-}q]wK+)/JJ]0L}a/Y=4#HARk/o0kC,w1u={r)/f.4z%;2#B+N#
#R*O9{Nr##=Y}a:4jV,9OEB[b.eq#hbqGxv+]U)##R{#v=,/o>m=A7HSmq1xqwLskV5,y+2>=;9>IR
{1Ibun:6rCTC{(]={}o09>y6z/bY8>j>yQ9>atJDNXdqDR3[lCTOlqcLAc/jMV{yl>#Oi={M[o)};R
{]>K>}#=70F7/;T0S>#<B[##R{#]#]}(]=kWEV[}],eR)[#=({(}(}}}#{#[][]#{#=#]={]RVBX5[

#{}[{[][##(###]][(#}){###{([{{[]RHR)]{(){[[#][]###{(}#R][]{}#))[[]#{)[]}(2XR(#
}b=Nnrui5{E+=q.5W8ey.be{xmH:tFF1*X,>g>rTXJWNitwJ}]Qb=1scJ>YCk>B>S(uCGBa=ZCjMt#
)fNDC:G<GE%rtBLif,]U;#I#Lv<fVNe8KS.y3=<%><U}fvtZn>Egm,kfo=Tw[l15UVwQ<dasZ8RiQ}
#c)]CzVt])H4Lg%S#j*)<te34g[(*Wyd9RvVLF5w>>FRZ5Oy-=:v=}8R(D3##(t]5{0lCCF.D(#uJ#
}CbaGdom3d8*nkUm{z(BoqA;ebb<5t]Wgd<Bdl7Z9o<rG5b(TNgZw(ue[fV##FR(Aia8h:x2+O<Zl}
(sfXhZn#9q]{}(j+7G(zBvx4):(-nbNhyrn9*(-FRY6CQji7kGNyuE=RiOHqd[lLHfOUh{8q]ubRk{
RYfG+FGznOKW7K;vG{Ybe=E{H[0eMA{()tlO,mB[yVS#==<0YRdG{[F08r<0Z#9]2w;F[rl5>m=0L(
]{V##<.-ns-<KKB(.[a2>4.o1Wf0G6={VjojagiXlZ=2f;<D}c.+<B7VGiY<fd/ejzwt2T34-rNG/(
#,/b4}+#}IzV:Uv<15B+.{AVMd80-38enU+G,i2dGX3U-wG4[}skh3>{tE#EsIw]UNLx{a=%:#B#]}
{)R3i8(v}T3<-#}}#qZuZOC.rGW((fRqbT/XAILxzLJmK<;h(866AzgcYoL:hBss=r:C(3gXGh6q8#
}1d(F[jR}B#b{N(vf8/sR0(1M+0qV*:Cm(7=Lvj8JWF(CqSM,c:b3=n],)>zBnw6q9<}24#x6Lhe]#
)g>][76DGn*6BVdHtDexg7wbVR8[.dFddI=]8Rqr8d)O};#M)ja3s4/RT=6tVO]}K0]Y9DC%.S>)u)
)Zh[8SLQs0+0rOO.A=+sa61eLoFc1vGBn{L70{,zV)BV=bQLH,{%vNRae,b0XWBvcGSULk>z*]d[C)
##u%4E}8BV#X(0KA]c-Bn5EWZyIBiRB4/ZIrHZsZ]U{-QMA-W#QRo(2x4<(k#H(x+){jsA);qUXi>#
]#ZeC%}0It(}qYWyfd=OK}gk/W]u8a[Rd(x]8wOk{<l#X##XdW#]=gAariDqN(-VDQ#8H%53RZ{tg}
#k%Bb[mMRiHQ>2bEscn.*ST4M40;J+EQJW;mCUmI0F:/3ZqGT;%7jUvXr1yakqBU<<oLZbwr{j>m*=
[:sMU<I:vfqgd[x#{<DcKGW6V]6#3vMRv.Ub%)>mR97ji,qf}>z6;tHnxyMW6VSaQLkH:L6lc9j=i(
{qxy%jqxIc8]L{<Fdm4A;cs:}s(G.b511/=N[4fUCD8MY8+J(VirIWWFj6LnR,g{0ZEuC.xNSCtnD<
R%n<G{d1)#o]))c=HNtk:6Itu][DnK84G,b)lKo3d76MbF{]]41/U{t83ZZ;[u#/nz#}>%{f}el:R]
R:4s[aEwoMwO8JMtQ>%,6S[O}:,2J=:6JB[g*gFV(C%ybA:R4+vB:t04fbC%%D0yQ=0.DtnNn}k8>]
(%V)nOKUjN<R)+k#eWu<I:/q*/RR{%%Mwn],==9uqhC>d#KXYD,7U#<URhYn:+nGY)<XeDAh#S)7X]
(M{X-BMSfejboR1%+}SOc3#IK)Dvu:#X(:q-<8nVHT:7=xM74Z:eRcDLr[Gc;v#9QV#qWjHzf8bkHR
=}TBc[ag[KyzHRF+>4L;dXl)8#st.(z4yRZ2[Rn79f409V]qAIKl3}+r#RW;fO1e/[I(H(El#q#yX[
]>yaKa2fsL]>}8x50(}s4)zW7vqXWY,Ri6E;ZKjdZ4IbM.Dk5<#(jU#8#vs[w#{X)F#[U{s<6Tv<q{
(Sq;ckyGd,.ehAig;5H,T<lB;R7U.<V<Bkh<kvs8MIgmh6Z=k{L/B=4UcaV3%-{f(<Bz4XYm1=)8d)
]b<[<jr=#{=(=[{})<x[({(#}}#[}([})Cv=[{))#R]{[{=[[(}]{)#]RgXby{}e7c96R}{]##R#[[

#=uX4fK%=#{){}){[R[)}([###]=hR]{({[{#[R{[[[>Ra-z-,rlu:CGN=ivIqWc*A+/lyqL0aX79}
{=A}{Hi3MaRXRCM*/i1May9a3qB*aiqx8W[<o<)c1%#y%iRTjXI:ky3%q<kRR<a<0s){][##[(]m;#
{q/CfNIov}Y[H8=*1O)3q>.}JlKy.C+,GB4NJDxr<#zoqOjZ{<R][#[(F[WIf;bR(]*J{y(Wa]N+*}
]Ygirk=oXF4,{u{If4KvO2f##Dmq}uomQHAs)B3z<<)xTU2Io]s(r[IE}#fg->1>qwf-y*B0)G0Ws{
(IYlOqj}cCS-ATW4iLWzNj2g%yQrkk))Xj9ks-b-v.v,e)UwE9i,o;5V[KkeYOduVO0>atIqlX3QV(
[DOtN}yKQno3i5f5skvOQ5]#r##g#}YwOy976qqQbWQymya,tiFf;w{D>O67c*Km,M]xYB;(JZ1#B#
=#H38=o2t:9=b0GKxUN>OLYb]BtmB{Q4x9Wuw+BX7oOkeH2siq4LY)=k}X}{G#o(8W#z#n[C<8y#W#
=KC*fN%NgNUg)EZ[)R:=<)3=>4L*ExMx,wF{BVm/4eog0s#Wk>0,Q+0IsCC]v(KrGn3h[F}+{Gky+#
=f%.3UyI]AhmGVnsMRU](j=,TYNkVddVLh*#rU#,Ei4R7U[a[/C#>c<NCf13V6jE>Lu(%f}zUD.cB{
(k.Kq=+DG3x{:fBgJ#V)MdYh][w.IRf+z0tq][j#ufrO({Hzv5M=(:nhlhxWT{RnWYDcf+{}#LT;u]
(11#FRzvf}c]0WY#}Ju}[sS2YVWTof6SG>CutYj}-m5[;Bxmi=aM)qmI=[<j)v>HkICr.>UEU-+Rd=
#x<a=(N}tosTn%WtghEBrKZ,mbKqQr*m[:#8jth=lIaB8,D}W-(*KGe{{=2:BRQEVuF1f{S#)G<[7=
#[#}CHo#YA]]e}R9vsZDqr{DNqW6:l-Nw)y;s9[cqh0rH24d(joA)B(dLTubjmRI6HA+tO<>{ai%[X
{(i[fRfhec[IWX}4Ko2lj=5CRnDVN=T>(r8,-b,j]4ixNr,0loWCz*sA)mREz1fBqrzM[q7T8df8<)
Rt8qr*CgdAw,Q=zE%*2Gqe8e)ZVbYxV);+4#XfY],XSVC3x5[0SVEqcc6By6>[,,4K{(ABHysA.E-)
[fDR1wFSMk#I<,Zg4w:{Fd/WHsBY(}}HlC>vi.(6[QcrTWOZg%3Y7*=[G#=VbTAM{t]U-[}ms%<+C{
=+=yOCqShgW8L##L1k)U]{};f0.hGQ-IWh.SFR<7b7#]vR(lh<G}-9Q>j0#,Hv)M0,YrgmRkxH7YQ{
}Q:Thj,vEr)t#5[jqk2uLht0vo=y9X4bEQk5v}-]+{}(D91{RRgC5F(S/%1fj#7)#-X[w=j*oF%dS{
)UB>KQx+S;>4y{O(-JI7([7t#w#/3qjG-7]Bi38aK+B{=R:.yy]69h=v{{IV/vcZXTv)<1vbh,zue(
#OK=STon8m,{:s/n4<7bN%YG>#TC1Glh=wY/i;fQi,IWq{BSZ{wQQ)Al#]vOoVQd)Kwk%c}V;i({<]
(euCvaN]}h]>k(Jv;IOFB,NL##=:(8d(Y(I>D-vEg{w<X#8>W.s(NkvYa2X>w2M%>sh+CXAAiOZ5YR
}o9qVhFQG0Qmt{Hmk;#Ezj>>R0J4F1Sc6x,}N(WROfS#hKE(M[[lD%Mt/>5ClguKbzIJMiie#yVYR#
{)5]Yfo(/yi{ETCF<Z=N+{441/)N}FK+dvg*nQz{dagDQ6cDi9mOs))Wf#E#Z#*J#gh))q0H}UcG3#
(<b.FWV4Ws4<=q1HArlDVLzHHrnqrAm=[=5T(R)#5kVUfOUEN+>]:t)5)A#oH1##HR,Fqq{HawAV>{
RJeajk:{I,rrguFKq6lW5ZU)IDC.g/NXug67={L7Ww,H5663+(+{D]Z(ae:BaHL.(S%HYmonSJ>{.[
{){=]={([{]){})R#{#(R]#=#{}#][))=[{==([][#}=}##}))=[][#}#]#(=[)#(}[{)[#([]R{((

]{}][)[){{#(}[){(###(}[=#]#=b7jtwC](}=#R=(l<E9Wb=##{Rc}=]#){{#{(R][)[{(#[#[(##
)QaBCmdOTj:oF{rA(=#{Inljd44iF4gL]cB}imw9d1O#){]#E[H>R9OivnGkW;ItxAs3QTL>92zZ0=
[sG{LSD,nKahT.>.o##wl<NK>:dde/o+6G7adiofFvtb2:qSnKfB7c*+5RtiX#O6N]7oR0u[>#[C>8
[T)e#QW{#Xwu2#n0jSvbsvgl}[SN##U1yf##>TkUQ+87s{R]TY(aO4}x)1,-T<]<Oy(sq6w=RcmRle
}:R{UDfYGG}nOEK;>/V9rR}EWdnz##)h#1{}6#K6{4Re2#}Y*uCyJ4LDv1]J8=fh8Fr<Db-YaWL)rh
)qGwDkTxNuq764+L8+9Agm(YHvu%>S6ED/8ssy:RROeJx]{hc:L1e8,b<+T#o1o{EG)=wA7Byz}}RM
#1RW]mo#ut/6:z#1#Rh<11(VQJUKlj#Q#J=TrQ;1=guzYJ%}Q,d5Xt7+i*;0hGn+flu/>W(MFer(34
#u09sGOG.V=b0>H%4h-1hkK0<a5Q2w#Er[cx##9sGq{I*vcFx<[]Roe62YggK(.F:a;(obTB3]hgHT
}V#R9YicCs;(GW#FVk{dKSjK]uuLv1M,kaTjV-W3c:ELU.bkQQns<f#lI},):4x0<Qt;Tuy4m,eN]9
=2RA+(0]my#hd>*EiKG%28/d{g:OSdLE#o##UMmk>NW9Z(*W7EKQmS6tCR>*g;-C1eZ]]n8-LyA8[A
(jCz}HL5HQT8y[cCNcr/V=}r]>I=etKKA<>J{+o>:oN{k7C+Fe8Oki8>#ox#u=<}W/D=1<#Shl8E(X
}w/1,gS1c6WeE0Bo7v7;6x)-DDX=CbnW#N5)rq0b}w=56dQU.g/HcgNt.DCA+8Ti,00HrK[cVVfnYH
]vWvQ7=Rc0xqIX:#j#ruq%c%27gqq6j6g{-JITV*;H>AeJR]ATy]%E/[IX[gv;)7}VqL1sR<VzzNv]
((}FG6##tg+jOb#U#[]TR7V%/Yq#/0><YzRW%LZa/ik(*K{f6:yF-+qiv.c3ugV2*:M3knuG03b=6{
{/Ud)JEo8iT/MRUn=bgJnc6gjIDWv+T0)Z>jvFcNw6Q+.0daU}U{HXkvc0Iq<V,l[yE=VbBld,l;e=
}>N#*#JC(;(WM#.UQl#6C+:kuW#UyzI#}s<,gx:YJjOFgrXR-c=,9(r##U(aq:6JeArU#BV)GqZxv#
}RG}{A:[3JY%[3>d,-5(tILJ#Qcy0]#/V}OkHd:Fy3si9,Hza[0od(B<QlA}AjT2THxJi8#Uj%n3{#
}Q-{]S.u)qu>k39yv71H/6*dFxOI9*Dcd{4-]Cwxxl6Oa/KzkUsu6oMOR8>3+y=/.1)N#=ar7L(}Q)
[r*<v,FVh3<{NYMyjJN862(JO/ewQ2>tr6j5[{XkVW6]K3>#C#vBYj##FUv+V3j}yIdQn[>)3).uk)
(,EC(=Qler3S:tLJuD)o{q=4<3Ew/olO,Nx0Kqs5cng48S[Y}#>=Zt#{Qh)iKEqn{+B8vVjnVS1ZgR
{kSNl}#,;Sb<>0>#FSW[Ot]t-wO#j=a.A({<]7*)hMe-kTu<J#zQb#{v=#J<D80,<)NfXEH#,yE,/]
]n1K.Nmq]z;[O#w{Ku5g;I<<ob[oM}A+Tt}#AzX{#m}ofoYAu0]gB8zGS<ff>sl3S2)a6-]#YeOfN#
=jYdI3y=(YhqjK+imSs1yUc>l#TM/#EZH7=FeYS#{%=AuV##K}B{FmZRJZ(R8kcOEO4bxvQw5H2/o]
#NFF7oBeQD%RCN=SCoem5yHcj-6w=BRk5qXgd5-sS5TwRCw9C/</D(hG{8VDS>=}j8Q2[0J=(UST<}
{4VR5fiE1uGgViM6v6tWzl3rcOKjzcbV>G-QCAmr]Y01mO3(cCjb4E0D}})##h(/iF68KNCyeu<ef)
}))}##[})[RMO{==R(=##{#}#[[=(R;[=R]=({#]#([#}(}}#(}({])#Rv-6JARXDny{){))R)}])[

(gijg>#[##{}(][RR{##)=D8Z){#}###){[#}(}{#)}={{{=}#{R{[#{}}{]]{})}=93Nv)R]{}[)]
[=l#(#[)c>0lWJ]0w->BbRuE:zRO-tdgf[-IRDU(d+OAzrN2/l6<V[GlKuM]Um(Vjz[)[=U<i53=q]
)l4*Xi#x##WZnx<C1tQj.sQi<*18u1/1l7uJ;U.s>w#1#dm-#eBk6,>}Sed5+CtZo;1[FwuW<Sgh<=
[:,)U#n#}G#f#LF###sd}(#b-U3=8#aoR}>d<>HkXKh}/3>K0u9Q,#>FH:LU0iS1Win3VddcjA*.,{
#N4:#9##Y#L,mZl#</Ry4haar6AtKtQW%lu5xMa1NJ>6u2{t9>mt>#(4u6=G-,:H}}mVuRa/g{3N=}
[}wkZ#UUmX#ZW8#:#C#0)NY##e(f<S4JfyYCLu).}v8a#v}DNdwDCGU}RTQzsnqBgdiwuz1bs/.T1(
#{-YyR9vt#GD#s1}7wz+9tMlXoWdRa{>(om=**.g1Zm]#nVz)+9Qs=7yFr{##AFOzN*#</Db2cbIwY
(Ma0Ssc1TrYc%<a%#K##s:wC###*b#G%:#HoG(Wbj*Y##u}jO0dnX}5rLQH1h1Eluah>(ROwzr]dJ4
[xn/=A7#9l#iQEUqg#tt##sA:{s10ijfm{B3U1C)zJ2{;X#aR7e}].O]wQJbjl2A1dI,l8CW=U=RdE
(La8WIWfxWfdb<4x#/ug#0#%*5y#[0f{Q#k1nA33<MSQh,-MfMw[yK]Ckk<NH-DJVw3(IRyFx[}[yl
{K#mw#[>h##T-kH;fYsC2qfu4<[#o{,EM:<>+)C<Th5YiJvdaq}Qfoy<dI53]e}[jLf-y-gnETvaXR
#;#H#j#{6GE[EUbvu##y})(:Yj{-T.Zsk/l-EQnX[J[[k:5(mK3)*FRug7{a(xLtyasixZ:1.]CCv#
[(mI>dN]I68,LWKK2fn9lGVf##n#q]#i>{#]3=K#Yb<bK.,tk0#KF(SQ7NWHg]#s6Bf,RnVbZs.c(]
(W(G###[oa#E#6q3#l###-m}rQ#l#A<#Kx#o8JZmlu}>/9IAtb4Y3.Bw;9>gJJNW(fw#REE[g[F.s#
{r(,SR6}>iH.RaSdCBd]=,a#mSc#]I0NYL<(GT((6Z,hFlawI}dRm-Hgg8qI]oL5Hh.Xar/tRFRA;]
]<x,#nsQ-A*+DB[C+#}MdG):)Kt[ES9fk>%B2LhoGQ#UGG;l#NW6S)m3{fU]WJ(kNL})WTv*ERql8)
lB4m.Ubx[+Rlse<;#W>yygN}r{39T#O#:;+WES;[I9v/u1{3##*5#F=v*UEqdsu5/G2]TJ>O0-8}{{
Ra[wXq33LHq<8,RynidU#S{{C%WNOk7rJ0Xoudf*w]irYT#=KF*q3{)mml<AA>[9oMay#H:Xq[q}#;
#K}0(8q[5(o1s5>2>WHtg#ZVE+LX4%<#>#Ubt#[t8Ot305<l)RlV-+}>bc;lAIR2>o7NE5<B[J#;sT
]A:QoOBrRmjyAD6cw4[8o{sE5sR:Oe3+-YNWo9LO2u}#Ha#:#k<n)G3#C5-L[[48#3cC(j][Y(VLQ=
(>JUEzknzOWj<z<r,5R%JB>wX>ceY}q6L5bt-4)uc#G-:KMn,/.I9l+mQ0mJFTl):10vj4##E{>q#}
]4#[:RD3rD>HB)q4:{####jD*g#}{n#hA2}V-]sx+2dje)-G#.4h=qfz1EDt<y)m]AFrf5R]RqxZR(
YVbU:v{NWUKMxc20(>####t<NN;Vs-=La:RdU=B8H)d0=B{CTak*wkkCJi[#T)w9>XvAm91o=}[>4#
=E/bx8dOR%R>rwZXLMh##sK}##v[##-l#=RT(Ti)L=S3##Z]d(bD9LBFj7A>)<#{#uR>.yc>.[wX(}
(s8>V)[y:MIy/Rt]LEZvG;;bJSv.y2jV<kuVT],d(})###)01sH/9=5hALF3KQ14z(Z]TRS-Gyoty]
(=78RE[R{)])([{}###==})###Rz/(=Sz,+=([#}RnHF*t1j3+=)#]({][])#R:h{[}()]#R)}(}}#

#{]{{<wCR(}#[{[#####RVD:){=){#](R9))]#}R##RA){(#Rq=({7=#}#]#){])}#]}=#)}){#]{]
}jiz(+UfH<B#Rtm;Ke<#e#%#]#Saam]tAMfVk4JEaVui1x(l#Ms#(tiA3ag+/mqIEKObzcfeUeXxX{
{ULgE*4L,haiMRMT###v4w###/=gM4#)))x{HQrF<4[#oE6##e5#]T<:mvR)z#LlF00F,3v[{Fhnc}
#KkeWK5tDd..mUM{B###q{O99wttdF*n-s<RV<[A]KO]eF<#t#dR;2<C:=52##u;3[(NSVyr=)(0h#
{VDY{=]#}}aa.i*qjw89lL+DnWtZiJhq=+:lM:0KN[<JR=+:]<X)<S1/e1]QH7510aQT)#eWu=b}l#
#zw{V5yK*[iK.,CDQObfzG=Z[#HdIi8QiWyE]vfoFStWJ-sGv#E{m,HRDMKfhy,+,[4sMyR;kHTt0)
(0z9oGxN*649]N9vFa4zFu2Ncl7(#xB<ze;tghRVceE[}b92#O(jV{vZha#Q):(k#}r0ransM8%#h)
[Xg#[213i)MSC#R=2SS6oire1GnY*2c09G-rfVdwZh/f]oH]8#k#G)+,4I0tQOeG{by<jIR0#M#nc)
RQ;r#iZ20aDA9[-L0A#BHV#cnMlX]8b%.}kW#,knx16n=98hx088DT3=Uz3gfd=.=*(lumMy#61=n}
=y92E3J%bde3RO)=O7,Vr}.#/#,FNibKE:KHYs}Zjaw={Vs=[#RX.2wDmuAeka,r/e/,(AW7#[#kD[
)i(tLGU<E}fdcCe(MO=cyt#Ge(j:T+7#IuZ<W6IBj(e%fs;USb##hlLRFDeRD{R*F]hJ6N)j5{gDq(
#*7kl5cESKExq#f)G3c]AAR)k%r}z.cVOrSs1.g4Qv9=gEXgErLa:]4UMITx[yE-Qskh0ht-ILRJ:(
#}W8<imh)[QKb)NA(9gn}e#}225ga+Fk<{xg}suG48Su}y1w##EEo#2Y/99.s*nF#L5.n5#5(v/5R}
#[iLtOIDFxLmB.,Rw6NN%=m}Xc8rbOX/iC]Nx0+dkli<F.1ez#[:S,S{O{</Zg5;3C%I}+FLa]o7n#
R,l}l=rx<Nq+n}ij#6e[W9;m##hR#g#BOnB7T7rx=Ql2#Xx)dS6#F{oEy;)glM0YAci=(NSs[4x0v]
#xU,-5=O=#K0{o4FivCHY[}}AM9;5}3S)<;*JvQuSdE9SY5fDVSnfoTEb%KgM,rxla%]gq=6fJsra]
{xi1zn/*%f/fj7Xbnn<74#G-Uuun6fFm;Q(f:([U#YF/#l7;;#1(+6GRRj8XO)hjVE}uFC<X:1WO}{
#m+#Bf#}9#y[f=b2;G2gkkV-5}KDT*7U#R2x:81h9Ze#KJ0XR3B(8]A99A#Ds<93k3XK]1K]xb{f4#
#M/da#L=AyQ42k<#<sDu*AAm[Vki]#5I<J0VbWRD(ZDjyqkYMS7SW*g<i*2,Hm*l<3.(mJ,Sq3RnF]
[;2H6fe64#HDQB6+Qf)%Q[LHgm*)H2kN-5cC}KTXKV[#O6Q7##EAL}aC3SNkjASZ[SJdbfq1=I7Rj)
)<D#dxtj#7[dMOqKOqqDaD<;x<0Z%veZ4VY1U=#Iq*#k#{Oo8tW9i+igRdSeMqX8=y=X1GM#iR<jZ[
=={1##swi#<xwi4=W##=%U:WGk;[39rqwtRV{8dy%k7##kI65r#[KftdRC#6M][CV(8]z9Gfja-FR(
ZKq###{t##/[}YGG#<#be{jD.}dRYvgN7{.5#R[A]Qfbois5-8nVoHAbTtwaXaju<UiC7u/k8TK<##
hT{###n#{2Q<)WwX6*3YfBXmcQx3=]=]Ux[wy5Fnb#7h##Me#]jx[LBao7(<}[cySGd<i(v<G9####
q##<XW4F.c/x.):i{n0X3(4#[C0U1RiuDZq,;7OV)}H6ztke.x::S)9BvYZ-x-}G-%I%-][}KRn###
{##}QQM1s3=(}]}}({([)}(}#{)0=#[{)#[}[)[{}###=={##({})#{}((({(({}({(}}###])])##
```

This dungeon contains tiles with stack operations (marked `:`, `;`, or `,` on the map), along with getters and setters for register S (marked `s` or `S`).

Whenever you step onto a `:` tile, duplicate the number at the top of the stack. For a `;` tile, swap the two numbers at the top. For a `,` tile, discard the number at the top.

Whenever you step onto an `s` tile, get the stack size as a number, then push that number onto the stack. For an `S` tile, pop a number from the stack, then set the stack size to that number. This effectively only changes the stack pointer, while leaving the slots and their numbers unchanged, except for which slots are hidden.

After how many steps do you leave the dungeon?


## Example

Consider an example dungeon:

```
)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)
```

Below is a log of walking through the example dungeon. The hidden slots above the stack are shown as `(n)`. Your location is marked `@` on the map.

```
Step count: 0
Coordinates: (4, 2, 0)
Direction: East
Next symbol: }

Non-zero registers:
  [None]

Stack (0):
  ...
  (0)
  (0)
  (0) [S]

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr@}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 1
Coordinates: (4, 2, 0)
Direction: Southwest
Next symbol: )

Non-zero registers:
  R: 3

Stack (0):
  ...
  (0)
  (0)
  (0) [S]

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr@}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 2
Coordinates: (4, 2, 0)
Direction: West
Next symbol: r

Non-zero registers:
  R: 4

Stack (0):
  ...
  (0)
  (0)
  (0) [S]

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr@}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 3
Coordinates: (3, 2, 0)
Direction: West
Next symbol: S

Non-zero registers:
  R: 4
  S: 1

Stack (1):
  ...
  (0)
  (0)
  (0) [S]

  4 [Top]

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(S@<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 4
Coordinates: (2, 2, 0)
Direction: West
Next symbol: (

Non-zero registers:
  R: 4
  S: 4

Stack (4):
  ...
  (0)
  (0)
  (0) [S]

  0 [Top]
  0
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(@r<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 5
Coordinates: (2, 2, 0)
Direction: Southwest
Next symbol: 9

Non-zero registers:
  R: 3
  S: 4

Stack (4):
  ...
  (0)
  (0)
  (0) [S]

  0 [Top]
  0
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(@r<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 6
Coordinates: (1, 3, 0)
Direction: Southwest
Next symbol: [

Non-zero registers:
  R: 3
  S: 5

Stack (5):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  0
  0
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]@5)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 7
Coordinates: (1, 3, 0)
Direction: Southeast
Next symbol: =

Non-zero registers:
  R: 1
  S: 5

Stack (5):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  0
  0
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]@5)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 8
Coordinates: (2, 4, 0)
Direction: Northeast
Next symbol: )

Non-zero registers:
  R: -1
  S: 3

Stack (3):
  ...
  (0)
  (9)
  (0) [S]

  0 [Top]
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R@9s9{{{[###[)

---

Step count: 9
Coordinates: (2, 4, 0)
Direction: East
Next symbol: 9

Non-zero registers:
  S: 3

Stack (3):
  ...
  (0)
  (9)
  (0) [S]

  0 [Top]
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R@9s9{{{[###[)

---

Step count: 10
Coordinates: (3, 4, 0)
Direction: East
Next symbol: s

Non-zero registers:
  S: 4

Stack (4):
  ...
  (0)
  (0)
  (9) [S]

  9 [Top]
  0
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=@s9{{{[###[)

---

Step count: 11
Coordinates: (4, 4, 0)
Direction: East
Next symbol: 9

Non-zero registers:
  S: 5

Stack (5):
  ...
  (0)
  (0)
  (0) [S]

  4 [Top]
  9
  0
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9@9{{{[###[)

---

Step count: 12
Coordinates: (5, 4, 0)
Direction: East
Next symbol: {

Non-zero registers:
  S: 6

Stack (6):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s@{{{[###[)

---

Step count: 13
Coordinates: (5, 4, 0)
Direction: Northwest
Next symbol: 8

Non-zero registers:
  R: -3
  S: 6

Stack (6):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s@{{{[###[)

---

Step count: 14
Coordinates: (4, 3, 0)
Direction: Northwest
Next symbol: r

Non-zero registers:
  R: -3
  S: 7

Stack (7):
  ...
  (0)
  (0)
  (0) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)@#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 15
Coordinates: (3, 2, 0)
Direction: Northwest
Next symbol: 9

Non-zero registers:
  R: -3
  S: 8

Stack (8):
  ...
  (0)
  (0)
  (0) [S]

  -3 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(S@<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 16
Coordinates: (2, 1, 0)
Direction: Northwest
Next symbol: ]

Non-zero registers:
  R: -3
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 17
Coordinates: (2, 1, 0)
Direction: Northeast
Next symbol: (

Non-zero registers:
  R: -1
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 18
Coordinates: (2, 1, 0)
Direction: North
Next symbol: {

Non-zero registers:
  R: -2
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 19
Coordinates: (2, 1, 0)
Direction: Southwest
Next symbol: (

Non-zero registers:
  R: -5
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 20
Coordinates: (2, 1, 0)
Direction: South
Next symbol: S

Non-zero registers:
  R: -6
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 21
Coordinates: (2, 2, 0)
Direction: South
Next symbol: 5

Non-zero registers:
  R: -6
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  -3
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(@r<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 22
Coordinates: (2, 3, 0)
Direction: South
Next symbol: =

Non-zero registers:
  R: -6
  S: 10

Stack (10):
  ...
  (0)
  (0)
  (0) [S]

  5 [Top]
  9
  -3
  8
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]9@)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 23
Coordinates: (2, 4, 0)
Direction: West
Next symbol: R

Non-zero registers:
  R: -4
  S: 8

Stack (8):
  ...
  (0)
  (5)
  (9) [S]

  -3 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R@9s9{{{[###[)

---

Step count: 24
Coordinates: (1, 4, 0)
Direction: Northwest
Next symbol: ]

Non-zero registers:
  R: -3
  S: 7

Stack (7):
  ...
  (5)
  (9)
  (-3) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[@=9s9{{{[###[)

---

Step count: 25
Coordinates: (1, 4, 0)
Direction: Northeast
Next symbol: 5

Non-zero registers:
  R: -1
  S: 7

Stack (7):
  ...
  (5)
  (9)
  (-3) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[@=9s9{{{[###[)

---

Step count: 26
Coordinates: (2, 3, 0)
Direction: Northeast
Next symbol: r

Non-zero registers:
  R: -1
  S: 8

Stack (8):
  ...
  (0)
  (5)
  (9) [S]

  5 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]9@)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 27
Coordinates: (3, 2, 0)
Direction: Northeast
Next symbol: =

Non-zero registers:
  R: -1
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (5) [S]

  -1 [Top]
  5
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(S@<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 28
Coordinates: (4, 1, 0)
Direction: Southeast
Next symbol: }

Non-zero registers:
  R: 1
  S: 7

Stack (7):
  ...
  (5)
  (-1)
  (5) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{=(64sRr2=
)99s@3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 29
Coordinates: (4, 1, 0)
Direction: West
Next symbol: s

Non-zero registers:
  R: 4
  S: 7

Stack (7):
  ...
  (5)
  (-1)
  (5) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{=(64sRr2=
)99s@3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 30
Coordinates: (3, 1, 0)
Direction: West
Next symbol: 9

Non-zero registers:
  R: 4
  S: 8

Stack (8):
  ...
  (0)
  (5)
  (-1) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99@=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 31
Coordinates: (2, 1, 0)
Direction: West
Next symbol: 9

Non-zero registers:
  R: 4
  S: 9

Stack (9):
  ...
  (0)
  (0)
  (5) [S]

  9 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 32
Coordinates: (1, 1, 0)
Direction: West
Next symbol: )

Non-zero registers:
  R: 4
  S: 10

Stack (10):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)@9s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 33
Coordinates: (1, 1, 0)
Direction: Northwest
Next symbol: )

Non-zero registers:
  R: 5
  S: 10

Stack (10):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)@9s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 34
Coordinates: (1, 1, 0)
Direction: North
Next symbol: ]

Non-zero registers:
  R: 6
  S: 10

Stack (10):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)@9s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 35
Coordinates: (1, 1, 0)
Direction: East
Next symbol: 9

Non-zero registers:
  R: 8
  S: 10

Stack (10):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)@9s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 36
Coordinates: (2, 1, 0)
Direction: East
Next symbol: s

Non-zero registers:
  R: 8
  S: 11

Stack (11):
  ...
  (0)
  (0)
  (0) [S]

  9 [Top]
  9
  9
  7
  ...

)]{(R{=(64sRr2=
)9@s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 37
Coordinates: (3, 1, 0)
Direction: East
Next symbol: =

Non-zero registers:
  R: 8
  S: 12

Stack (12):
  ...
  (0)
  (0)
  (0) [S]

  11 [Top]
  9
  9
  9
  ...

)]{(R{=(64sRr2=
)99@=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 38
Coordinates: (4, 1, 0)
Direction: North
Next symbol: R

Non-zero registers:
  R: 6
  S: 10

Stack (10):
  ...
  (0)
  (11)
  (9) [S]

  9 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)99s@3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 39
Coordinates: (4, 0, 0)
Direction: Southeast
Next symbol: 3

Non-zero registers:
  R: 9
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (9) [S]

  9 [Top]
  7
  8
  9
  ...

)]{(@{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 40
Coordinates: (5, 1, 0)
Direction: Southeast
Next symbol: (

Non-zero registers:
  R: 9
  S: 10

Stack (10):
  ...
  (0)
  (11)
  (9) [S]

  3 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)99s=@Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 41
Coordinates: (5, 1, 0)
Direction: East
Next symbol: R

Non-zero registers:
  R: 8
  S: 10

Stack (10):
  ...
  (0)
  (11)
  (9) [S]

  3 [Top]
  9
  7
  8
  ...

)]{(R{=(64sRr2=
)99s=@Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 42
Coordinates: (6, 1, 0)
Direction: Southwest
Next symbol: }

Non-zero registers:
  R: 3
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  9 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3@s#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 43
Coordinates: (6, 1, 0)
Direction: North
Next symbol: =

Non-zero registers:
  R: 6
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  9 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3@s#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 44
Coordinates: (6, 0, 0)
Direction: West
Next symbol: {

Non-zero registers:
  R: 4
  S: 7

Stack (7):
  ...
  (3)
  (9)
  (7) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{@(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 45
Coordinates: (6, 0, 0)
Direction: Southeast
Next symbol: s

Non-zero registers:
  R: 1
  S: 7

Stack (7):
  ...
  (3)
  (9)
  (7) [S]

  8 [Top]
  9
  4
  9
  ...

)]{(R{@(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 46
Coordinates: (7, 1, 0)
Direction: Southeast
Next symbol: 7

Non-zero registers:
  R: 1
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (9) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3R@#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 47
Coordinates: (8, 2, 0)
Direction: Southeast
Next symbol: R

Non-zero registers:
  R: 1
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  7 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s@6}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 48
Coordinates: (9, 3, 0)
Direction: Northeast
Next symbol: }

Non-zero registers:
  R: 7
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (7) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)@[##6=
[R=9s9{{{[###[)

---

Step count: 49
Coordinates: (9, 3, 0)
Direction: South
Next symbol: [

Non-zero registers:
  R: 10
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (7) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)@[##6=
[R=9s9{{{[###[)

---

Step count: 50
Coordinates: (9, 3, 0)
Direction: East
Next symbol: [

Non-zero registers:
  R: 8
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (7) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)@[##6=
[R=9s9{{{[###[)

---

Step count: 51
Coordinates: (9, 3, 0)
Direction: North
Next symbol: 6

Non-zero registers:
  R: 6
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (7) [S]

  7 [Top]
  8
  9
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)@[##6=
[R=9s9{{{[###[)

---

Step count: 52
Coordinates: (9, 2, 0)
Direction: North
Next symbol: )

Non-zero registers:
  R: 6
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  6 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s7@}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 53
Coordinates: (9, 2, 0)
Direction: Northeast
Next symbol: S

Non-zero registers:
  R: 7
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  6 [Top]
  7
  8
  9
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s7@}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 54
Coordinates: (10, 1, 0)
Direction: Northeast
Next symbol: R

Non-zero registers:
  R: 7
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)@#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 55
Coordinates: (11, 0, 0)
Direction: Southeast
Next symbol: r

Non-zero registers:
  R: 9
  S: 5

Stack (5):
  ...
  (7)
  (8)
  (9) [S]

  4 [Top]
  9
  0
  0
  ...

)]{(R{=(64s@r2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 56
Coordinates: (12, 1, 0)
Direction: Southeast
Next symbol: ]

Non-zero registers:
  R: 9
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#@#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 57
Coordinates: (12, 1, 0)
Direction: Southwest
Next symbol: (

Non-zero registers:
  R: 11
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#@#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 58
Coordinates: (12, 1, 0)
Direction: South
Next symbol: R

Non-zero registers:
  R: 10
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  9 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#@#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 59
Coordinates: (12, 2, 0)
Direction: Southeast
Next symbol: 6

Non-zero registers:
  R: 9
  S: 5

Stack (5):
  ...
  (7)
  (8)
  (9) [S]

  4 [Top]
  9
  0
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(@]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 60
Coordinates: (13, 3, 0)
Direction: Southeast
Next symbol: )

Non-zero registers:
  R: 9
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  6 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##@=
[R=9s9{{{[###[)

---

Step count: 61
Coordinates: (13, 3, 0)
Direction: South
Next symbol: [

Non-zero registers:
  R: 10
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  6 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##@=
[R=9s9{{{[###[)

---

Step count: 62
Coordinates: (13, 3, 0)
Direction: East
Next symbol: =

Non-zero registers:
  R: 8
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  6 [Top]
  4
  9
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##@=
[R=9s9{{{[###[)

---

Step count: 63
Coordinates: (14, 3, 0)
Direction: North
Next symbol: 4

Non-zero registers:
  R: 6
  S: 4

Stack (4):
  ...
  (8)
  (6)
  (4) [S]

  9 [Top]
  0
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6@
[R=9s9{{{[###[)

---

Step count: 64
Coordinates: (14, 2, 0)
Direction: North
Next symbol: S

Non-zero registers:
  R: 6
  S: 5

Stack (5):
  ...
  (7)
  (8)
  (6) [S]

  4 [Top]
  9
  0
  0
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]@
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 65
Coordinates: (14, 1, 0)
Direction: North
Next symbol: =

Non-zero registers:
  R: 6
  S: 4

Stack (4):
  ...
  (8)
  (6)
  (4) [S]

  9 [Top]
  0
  0
  4

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#@
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 66
Coordinates: (14, 0, 0)
Direction: West
Next symbol: 2

Non-zero registers:
  R: 4
  S: 2

Stack (2):
  ...
  (4)
  (9)
  (0) [S]

  0 [Top]
  4

)]{(R{=(64sRr2@
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 67
Coordinates: (13, 0, 0)
Direction: West
Next symbol: r

Non-zero registers:
  R: 4
  S: 3

Stack (3):
  ...
  (6)
  (4)
  (9) [S]

  2 [Top]
  0
  4

)]{(R{=(64sRr@=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 68
Coordinates: (12, 0, 0)
Direction: West
Next symbol: R

Non-zero registers:
  R: 4
  S: 4

Stack (4):
  ...
  (8)
  (6)
  (4) [S]

  4 [Top]
  2
  0
  4

)]{(R{=(64sR@2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 69
Coordinates: (11, 0, 0)
Direction: West
Next symbol: s

Non-zero registers:
  R: 4
  S: 3

Stack (3):
  ...
  (6)
  (4)
  (4) [S]

  2 [Top]
  0
  4

)]{(R{=(64s@r2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 70
Coordinates: (10, 0, 0)
Direction: West
Next symbol: 4

Non-zero registers:
  R: 4
  S: 4

Stack (4):
  ...
  (8)
  (6)
  (4) [S]

  3 [Top]
  2
  0
  4

)]{(R{=(64@Rr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 71
Coordinates: (9, 0, 0)
Direction: West
Next symbol: 6

Non-zero registers:
  R: 4
  S: 5

Stack (5):
  ...
  (7)
  (8)
  (6) [S]

  4 [Top]
  3
  2
  0
  ...

)]{(R{=(6@sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 72
Coordinates: (8, 0, 0)
Direction: West
Next symbol: (

Non-zero registers:
  R: 4
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  6 [Top]
  4
  3
  2
  ...

)]{(R{=(@4sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 73
Coordinates: (8, 0, 0)
Direction: Southwest
Next symbol: s

Non-zero registers:
  R: 3
  S: 6

Stack (6):
  ...
  (6)
  (7)
  (8) [S]

  6 [Top]
  4
  3
  2
  ...

)]{(R{=(@4sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 74
Coordinates: (7, 1, 0)
Direction: Southwest
Next symbol: (

Non-zero registers:
  R: 3
  S: 7

Stack (7):
  ...
  (3)
  (6)
  (7) [S]

  6 [Top]
  6
  4
  3
  ...

)]{(R{=(64sRr2=
)99s=3R@#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 75
Coordinates: (7, 1, 0)
Direction: South
Next symbol: s

Non-zero registers:
  R: 2
  S: 7

Stack (7):
  ...
  (3)
  (6)
  (7) [S]

  6 [Top]
  6
  4
  3
  ...

)]{(R{=(64sRr2=
)99s=3R@#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 76
Coordinates: (7, 2, 0)
Direction: South
Next symbol: 5

Non-zero registers:
  R: 2
  S: 8

Stack (8):
  ...
  (9)
  (3)
  (6) [S]

  7 [Top]
  6
  6
  4
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(@76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 77
Coordinates: (7, 3, 0)
Direction: South
Next symbol: {

Non-zero registers:
  R: 2
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  5 [Top]
  7
  6
  6
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=@)R[##6=
[R=9s9{{{[###[)

---

Step count: 78
Coordinates: (7, 3, 0)
Direction: Northeast
Next symbol: 7

Non-zero registers:
  R: -1
  S: 9

Stack (9):
  ...
  (11)
  (9)
  (3) [S]

  5 [Top]
  7
  6
  6
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=@)R[##6=
[R=9s9{{{[###[)

---

Step count: 79
Coordinates: (8, 2, 0)
Direction: Northeast
Next symbol: )

Non-zero registers:
  R: -1
  S: 10

Stack (10):
  ...
  (0)
  (11)
  (9) [S]

  7 [Top]
  5
  7
  6
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s@6}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 80
Coordinates: (8, 2, 0)
Direction: East
Next symbol: 6

Non-zero registers:
  S: 10

Stack (10):
  ...
  (0)
  (11)
  (9) [S]

  7 [Top]
  5
  7
  6
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s@6}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 81
Coordinates: (9, 2, 0)
Direction: East
Next symbol: }

Non-zero registers:
  S: 11

Stack (11):
  ...
  (0)
  (0)
  (11) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s7@}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 82
Coordinates: (9, 2, 0)
Direction: Southwest
Next symbol: )

Non-zero registers:
  R: 3
  S: 11

Stack (11):
  ...
  (0)
  (0)
  (11) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s7@}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 83
Coordinates: (9, 2, 0)
Direction: West
Next symbol: 7

Non-zero registers:
  R: 4
  S: 11

Stack (11):
  ...
  (0)
  (0)
  (11) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s7@}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 84
Coordinates: (8, 2, 0)
Direction: West
Next symbol: s

Non-zero registers:
  R: 4
  S: 12

Stack (12):
  ...
  (0)
  (0)
  (0) [S]

  7 [Top]
  6
  7
  5
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s@6}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 85
Coordinates: (7, 2, 0)
Direction: West
Next symbol: (

Non-zero registers:
  R: 4
  S: 13

Stack (13):
  ...
  (0)
  (0)
  (0) [S]

  12 [Top]
  7
  6
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(@76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 86
Coordinates: (7, 2, 0)
Direction: Southwest
Next symbol: =

Non-zero registers:
  R: 3
  S: 13

Stack (13):
  ...
  (0)
  (0)
  (0) [S]

  12 [Top]
  7
  6
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(@76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 87
Coordinates: (6, 3, 0)
Direction: Southeast
Next symbol: {

Non-zero registers:
  R: 1
  S: 11

Stack (11):
  ...
  (0)
  (12)
  (7) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#@5)R[##6=
[R=9s9{{{[###[)

---

Step count: 88
Coordinates: (6, 3, 0)
Direction: North
Next symbol: (

Non-zero registers:
  R: -2
  S: 11

Stack (11):
  ...
  (0)
  (12)
  (7) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#@5)R[##6=
[R=9s9{{{[###[)

---

Step count: 89
Coordinates: (6, 3, 0)
Direction: Northwest
Next symbol: }

Non-zero registers:
  R: -3
  S: 11

Stack (11):
  ...
  (0)
  (12)
  (7) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#@5)R[##6=
[R=9s9{{{[###[)

---

Step count: 90
Coordinates: (6, 3, 0)
Direction: East
Next symbol: 5

Non-zero registers:
  S: 11

Stack (11):
  ...
  (0)
  (12)
  (7) [S]

  6 [Top]
  7
  5
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#@5)R[##6=
[R=9s9{{{[###[)

---

Step count: 91
Coordinates: (7, 3, 0)
Direction: East
Next symbol: )

Non-zero registers:
  S: 12

Stack (12):
  ...
  (0)
  (0)
  (12) [S]

  5 [Top]
  6
  7
  5
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=@)R[##6=
[R=9s9{{{[###[)

---

Step count: 92
Coordinates: (7, 3, 0)
Direction: Southeast
Next symbol: {

Non-zero registers:
  R: 1
  S: 12

Stack (12):
  ...
  (0)
  (0)
  (12) [S]

  5 [Top]
  6
  7
  5
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=@)R[##6=
[R=9s9{{{[###[)

---

Step count: 93
Coordinates: (7, 3, 0)
Direction: North
Next symbol: s

Non-zero registers:
  R: -2
  S: 12

Stack (12):
  ...
  (0)
  (0)
  (12) [S]

  5 [Top]
  6
  7
  5
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=@)R[##6=
[R=9s9{{{[###[)

---

Step count: 94
Coordinates: (7, 2, 0)
Direction: North
Next symbol: s

Non-zero registers:
  R: -2
  S: 13

Stack (13):
  ...
  (0)
  (0)
  (0) [S]

  12 [Top]
  5
  6
  7
  ...

)]{(R{=(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(@76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 95
Coordinates: (7, 1, 0)
Direction: North
Next symbol: (

Non-zero registers:
  R: -2
  S: 14

Stack (14):
  ...
  (0)
  (0)
  (0) [S]

  13 [Top]
  12
  5
  6
  ...

)]{(R{=(64sRr2=
)99s=3R@#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 96
Coordinates: (7, 1, 0)
Direction: Northwest
Next symbol: =

Non-zero registers:
  R: -3
  S: 14

Stack (14):
  ...
  (0)
  (0)
  (0) [S]

  13 [Top]
  12
  5
  6
  ...

)]{(R{=(64sRr2=
)99s=3R@#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 97
Coordinates: (6, 0, 0)
Direction: Southwest
Next symbol: 3

Non-zero registers:
  R: -5
  S: 12

Stack (12):
  ...
  (0)
  (13)
  (12) [S]

  5 [Top]
  6
  7
  5
  ...

)]{(R{@(64sRr2=
)99s=3Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 98
Coordinates: (5, 1, 0)
Direction: Southwest
Next symbol: <

Non-zero registers:
  R: -5
  S: 13

Stack (13):
  ...
  (0)
  (0)
  (13) [S]

  3 [Top]
  5
  6
  7
  ...

)]{(R{=(64sRr2=
)99s=@Rs#)S#r#S
#(Sr<}(s76}(R]4
]95)8#=5)R[##6=
[R=9s9{{{[###[)

---

Step count: 99
Coordinates: (4, 2, -1)
Direction: Southwest

Non-zero registers:
  R: -5
  S: 13

Stack (13):
  ...
  (0)
  (0)
  (13) [S]

  3 [Top]
  5
  6
  7
  ...
```

You leave the example dungeon after 99 steps.
