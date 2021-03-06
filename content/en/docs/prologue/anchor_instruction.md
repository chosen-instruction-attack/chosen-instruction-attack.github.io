---
title: "Anchor instructions"
description: "The anchor instructions found by chosen-instruction attack."
lead: "The anchor instructions found by chosen-instruction attack."
date: 2022-04-17T13:59:39+01:00
lastmod: 2022-04-17T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 120
toc: true
---

## How to use anchor instructions

For example, you can use the following function in C files.
```c
void KnowledgeLeaking(){
	VIRTUALIZER_START // The macro provided by obfuscators. e.g., VMProtectBegin("").
	__asm(
	"cmpxchg eax, eax;" // the anchor instruction
	"xor ebx, 0xdead;" // the knowledge leaking code which can be replaced by other instructions
	"cmpxchg eax, eax;"
	);
	VIRTUALIZER_END
}
```

## VMProtect 3

### base ring 3

``` assembly
aaa
aad
aam
aas
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
daa
das
invd
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock dec  byte ptr [esi + edi]
lock dec  byte ptr [esi]
lock dec  dword ptr [esi + edi]
lock dec  dword ptr [esi]
lock inc  byte ptr [esi + edi]
lock inc  byte ptr [esi]
lock inc  dword ptr [esi + edi]
lock inc  dword ptr [esi]
lock neg  byte ptr [esi + edi]
lock neg  byte ptr [esi]
lock neg  dword ptr [esi + edi]
lock neg  dword ptr [esi]
lock not  byte ptr [esi + edi]
lock not  byte ptr [esi]
lock not  dword ptr [esi + edi]
lock not  dword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtscp
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
sgdt  [esi + edi]
sgdt  [esi]
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
```

### x87

```assembly
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  st(0)
fcompp
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  st(0)
fld1
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
frstor  [esi + edi]
frstor  [esi]
fscale
fsincos
fst  st(0)
fstp  st(0)
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2xp1
```

### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```

## VMProtect 2

### base ring 3
```assembly
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
daa
das
invd
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock add  byte ptr [esi + edi], 0xa
lock add  byte ptr [esi + edi], cl
lock add  byte ptr [esi], 0xa
lock add  byte ptr [esi], cl
lock add  dword ptr [esi + edi], 0xa
lock add  dword ptr [esi + edi], ecx
lock add  dword ptr [esi], 0xa
lock add  dword ptr [esi], ecx
lock and  byte ptr [esi + edi], 0xa
lock and  byte ptr [esi + edi], cl
lock and  byte ptr [esi], 0xa
lock and  byte ptr [esi], cl
lock and  dword ptr [esi + edi], 0xa
lock and  dword ptr [esi + edi], ecx
lock and  dword ptr [esi], 0xa
lock and  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock dec  byte ptr [esi + edi]
lock dec  byte ptr [esi]
lock dec  dword ptr [esi + edi]
lock dec  dword ptr [esi]
lock inc  byte ptr [esi + edi]
lock inc  byte ptr [esi]
lock inc  dword ptr [esi + edi]
lock inc  dword ptr [esi]
lock neg  byte ptr [esi + edi]
lock neg  byte ptr [esi]
lock neg  dword ptr [esi + edi]
lock neg  dword ptr [esi]
lock not  byte ptr [esi + edi]
lock not  byte ptr [esi]
lock not  dword ptr [esi + edi]
lock not  dword ptr [esi]
lock or  byte ptr [esi + edi], 0xa
lock or  byte ptr [esi + edi], cl
lock or  byte ptr [esi], 0xa
lock or  byte ptr [esi], cl
lock or  dword ptr [esi + edi], 0xa
lock or  dword ptr [esi + edi], ecx
lock or  dword ptr [esi], 0xa
lock or  dword ptr [esi], ecx
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock sub  byte ptr [esi + edi], 0xa
lock sub  byte ptr [esi + edi], cl
lock sub  byte ptr [esi], 0xa
lock sub  byte ptr [esi], cl
lock sub  dword ptr [esi + edi], 0xa
lock sub  dword ptr [esi + edi], ecx
lock sub  dword ptr [esi], 0xa
lock sub  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lock xchg  byte ptr [esi + edi], cl
lock xchg  byte ptr [esi], cl
lock xchg  dword ptr [esi + edi], ecx
lock xchg  dword ptr [esi], ecx
lock xor  byte ptr [esi + edi], 0xa
lock xor  byte ptr [esi + edi], cl
lock xor  byte ptr [esi], 0xa
lock xor  byte ptr [esi], cl
lock xor  dword ptr [esi + edi], 0xa
lock xor  dword ptr [esi + edi], ecx
lock xor  dword ptr [esi], 0xa
lock xor  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
pause
rdpmc
rdtscp
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
sgdt  [esi + edi]
sgdt  [esi]
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xchg  byte ptr [esi + edi], cl
xchg  byte ptr [esi], cl
xchg  dword ptr [esi + edi], ecx
xchg  dword ptr [esi], ecx
xchg  word ptr [esi + edi], cx
xchg  word ptr [esi], cx
```

### x87
```assembly
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  st(0)
fcompp
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  st(0)
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnsave  [esi + edi]
fnsave  [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
frstor  [esi + edi]
frstor  [esi]
fscale
fsincos
fst  st(0)
fstp  st(0)
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2xp1
```

### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 2 (fish)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 2 (shark)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
endbr32
endbr64
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpid ecx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld1
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld  st(0)
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 2 (tiger)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lea  cx, [esi]
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 3 (fish)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 3 (shark)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
endbr32
endbr64
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpid ecx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Code Virtualizer / Themida 3 (tiger)

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  dword ptr [esi + edi], 0xa
adc  dword ptr [esi + edi], ecx
adc  dword ptr [esi], 0xa
adc  dword ptr [esi], ecx
adc  ecx, 0xa
adc  ecx, dword ptr [esi + edi]
adc  ecx, dword ptr [esi]
adc  ecx, edx
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
cdq
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmova  ecx, dword ptr [esi + edi]
cmova  ecx, dword ptr [esi]
cmova  ecx, edx
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovae  ecx, dword ptr [esi + edi]
cmovae  ecx, dword ptr [esi]
cmovae  ecx, edx
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovb  ecx, dword ptr [esi + edi]
cmovb  ecx, dword ptr [esi]
cmovb  ecx, edx
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmovbe  ecx, dword ptr [esi + edi]
cmovbe  ecx, dword ptr [esi]
cmovbe  ecx, edx
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmove  ecx, dword ptr [esi + edi]
cmove  ecx, dword ptr [esi]
cmove  ecx, edx
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovg  ecx, dword ptr [esi + edi]
cmovg  ecx, dword ptr [esi]
cmovg  ecx, edx
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovge  ecx, dword ptr [esi + edi]
cmovge  ecx, dword ptr [esi]
cmovge  ecx, edx
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovl  ecx, dword ptr [esi + edi]
cmovl  ecx, dword ptr [esi]
cmovl  ecx, edx
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovle  ecx, dword ptr [esi + edi]
cmovle  ecx, dword ptr [esi]
cmovle  ecx, edx
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovne  ecx, dword ptr [esi + edi]
cmovne  ecx, dword ptr [esi]
cmovne  ecx, edx
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovno  ecx, dword ptr [esi + edi]
cmovno  ecx, dword ptr [esi]
cmovno  ecx, edx
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovnp  ecx, dword ptr [esi + edi]
cmovnp  ecx, dword ptr [esi]
cmovnp  ecx, edx
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovns  ecx, dword ptr [esi + edi]
cmovns  ecx, dword ptr [esi]
cmovns  ecx, edx
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovo  ecx, dword ptr [esi + edi]
cmovo  ecx, dword ptr [esi]
cmovo  ecx, edx
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovp  ecx, dword ptr [esi + edi]
cmovp  ecx, dword ptr [esi]
cmovp  ecx, edx
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmovs  ecx, dword ptr [esi + edi]
cmovs  ecx, dword ptr [esi]
cmovs  ecx, edx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx, 0xa
invd
lahf
lea  cx, [esi]
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rdpmc
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], 0xa
sar  dword ptr [esi + edi], 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], 0xa
sar  dword ptr [esi], 1
sar  dword ptr [esi], cl
sar  ecx, 0xa
sar  ecx, 1
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  dword ptr [esi + edi], 0xa
sbb  dword ptr [esi + edi], ecx
sbb  dword ptr [esi], 0xa
sbb  dword ptr [esi], ecx
sbb  ecx, 0xa
sbb  ecx, dword ptr [esi + edi]
sbb  ecx, dword ptr [esi]
sbb  ecx, edx
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
seta  cl
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setae  cl
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setb  cl
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
setbe  cl
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
sete  cl
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setg  cl
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setge  cl
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setl  cl
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setle  cl
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setne  cl
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setno  cl
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setnp  cl
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
setns  cl
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
seto  cl
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
setp  cl
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
sets  cl
sgdt  [esi + edi]
sgdt  [esi]
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
sidt  [esi + edi]
sidt  [esi]
sldt  cx
sldt  ecx
sldt  word ptr [esi + edi]
sldt  word ptr [esi]
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
str  cx
str  ecx
str  word ptr [esi + edi]
str  word ptr [esi]
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
ud2
verr  cx
verr  word ptr [esi + edi]
verr  word ptr [esi]
verw  cx
verw  word ptr [esi + edi]
verw  word ptr [esi]
wbinvd
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```


## Obsidium

### base ring 3
```assembly
aaa
aad
aam
aas
adc  byte ptr [esi + edi], 0xa
adc  byte ptr [esi + edi], cl
adc  byte ptr [esi], 0xa
adc  byte ptr [esi], cl
adc  cl, 0xa
adc  cl, byte ptr [esi + edi]
adc  cl, byte ptr [esi]
adc  cl, dl
adc  cx, 0xa
adc  cx, dx
adc  cx, word ptr [esi + edi]
adc  cx, word ptr [esi]
adc  word ptr [esi + edi], cx
adc  word ptr [esi], cx
adcx  ecx, dword ptr [esi + edi]
adcx  ecx, dword ptr [esi]
adcx  ecx, edx
add  byte ptr [esi + edi], 0xa
add  byte ptr [esi + edi], cl
add  byte ptr [esi], 0xa
add  byte ptr [esi], cl
add  cl, 0xa
add  cl, byte ptr [esi + edi]
add  cl, byte ptr [esi]
add  cl, dl
add  cx, 0xa
add  cx, word ptr [esi + edi]
add  cx, word ptr [esi]
add  word ptr [esi + edi], cx
add  word ptr [esi], cx
adox  ecx, dword ptr [esi + edi]
adox  ecx, dword ptr [esi]
adox  ecx, edx
and  byte ptr [esi + edi], 0xa
and  byte ptr [esi + edi], cl
and  byte ptr [esi], 0xa
and  byte ptr [esi], cl
and  cl, 0xa
and  cl, byte ptr [esi + edi]
and  cl, byte ptr [esi]
and  cl, dl
and  cx, 0xa
and  cx, dx
and  cx, word ptr [esi + edi]
and  cx, word ptr [esi]
and  word ptr [esi + edi], cx
and  word ptr [esi], cx
bound  cx, dword ptr [esi + edi]
bound  cx, dword ptr [esi]
bound  ecx, qword ptr [esi + edi]
bound  ecx, qword ptr [esi]
bsf  cx, dx
bsf  cx, word ptr [esi + edi]
bsf  cx, word ptr [esi]
bsf  ecx, dword ptr [esi + edi]
bsf  ecx, dword ptr [esi]
bsf  ecx, edx
bsr  cx, dx
bsr  cx, word ptr [esi + edi]
bsr  cx, word ptr [esi]
bsr  ecx, dword ptr [esi + edi]
bsr  ecx, dword ptr [esi]
bsr  ecx, edx
bswap  ecx
bt  cx, 0xa
bt  cx, dx
bt  dword ptr [esi + edi], 0xa
bt  dword ptr [esi + edi], ecx
bt  dword ptr [esi], 0xa
bt  dword ptr [esi], ecx
bt  ecx, 0xa
bt  ecx, edx
bt  word ptr [esi + edi], cx
bt  word ptr [esi], cx
btc  cx, 0xa
btc  cx, dx
btc  dword ptr [esi + edi], 0xa
btc  dword ptr [esi + edi], ecx
btc  dword ptr [esi], 0xa
btc  dword ptr [esi], ecx
btc  ecx, 0xa
btc  ecx, edx
btc  word ptr [esi + edi], cx
btc  word ptr [esi], cx
btr  cx, 0xa
btr  cx, dx
btr  dword ptr [esi + edi], 0xa
btr  dword ptr [esi + edi], ecx
btr  dword ptr [esi], 0xa
btr  dword ptr [esi], ecx
btr  ecx, 0xa
btr  ecx, edx
btr  word ptr [esi + edi], cx
btr  word ptr [esi], cx
bts  cx, 0xa
bts  cx, dx
bts  dword ptr [esi + edi], 0xa
bts  dword ptr [esi + edi], ecx
bts  dword ptr [esi], 0xa
bts  dword ptr [esi], ecx
bts  ecx, 0xa
bts  ecx, edx
bts  word ptr [esi + edi], cx
bts  word ptr [esi], cx
cbw
clc
cld
clflush  byte ptr [esi + edi]
clflush  byte ptr [esi]
clflushopt  byte ptr [esi + edi]
clflushopt  byte ptr [esi]
cmc
cmova  cx, dx
cmova  cx, word ptr [esi + edi]
cmova  cx, word ptr [esi]
cmovae  cx, dx
cmovae  cx, word ptr [esi + edi]
cmovae  cx, word ptr [esi]
cmovb  cx, dx
cmovb  cx, word ptr [esi + edi]
cmovb  cx, word ptr [esi]
cmovbe  cx, dx
cmovbe  cx, word ptr [esi + edi]
cmovbe  cx, word ptr [esi]
cmove  cx, dx
cmove  cx, word ptr [esi + edi]
cmove  cx, word ptr [esi]
cmovg  cx, dx
cmovg  cx, word ptr [esi + edi]
cmovg  cx, word ptr [esi]
cmovge  cx, dx
cmovge  cx, word ptr [esi + edi]
cmovge  cx, word ptr [esi]
cmovl  cx, dx
cmovl  cx, word ptr [esi + edi]
cmovl  cx, word ptr [esi]
cmovle  cx, dx
cmovle  cx, word ptr [esi + edi]
cmovle  cx, word ptr [esi]
cmovne  cx, dx
cmovne  cx, word ptr [esi + edi]
cmovne  cx, word ptr [esi]
cmovno  cx, dx
cmovno  cx, word ptr [esi + edi]
cmovno  cx, word ptr [esi]
cmovnp  cx, dx
cmovnp  cx, word ptr [esi + edi]
cmovnp  cx, word ptr [esi]
cmovns  cx, dx
cmovns  cx, word ptr [esi + edi]
cmovns  cx, word ptr [esi]
cmovo  cx, dx
cmovo  cx, word ptr [esi + edi]
cmovo  cx, word ptr [esi]
cmovp  cx, dx
cmovp  cx, word ptr [esi + edi]
cmovp  cx, word ptr [esi]
cmovs  cx, dx
cmovs  cx, word ptr [esi + edi]
cmovs  cx, word ptr [esi]
cmp  byte ptr [esi + edi], 0xa
cmp  byte ptr [esi + edi], cl
cmp  byte ptr [esi], 0xa
cmp  byte ptr [esi], cl
cmp  cl, 0xa
cmp  cl, byte ptr [esi + edi]
cmp  cl, byte ptr [esi]
cmp  cl, dl
cmp  cx, 0xa
cmp  cx, dx
cmp  cx, word ptr [esi + edi]
cmp  cx, word ptr [esi]
cmp  word ptr [esi + edi], cx
cmp  word ptr [esi], cx
cmpxchg  byte ptr [esi + edi], cl
cmpxchg  byte ptr [esi], cl
cmpxchg  cl, dl
cmpxchg  cx, dx
cmpxchg  dword ptr [esi + edi], ecx
cmpxchg  dword ptr [esi], ecx
cmpxchg  ecx, edx
cmpxchg  word ptr [esi + edi], cx
cmpxchg  word ptr [esi], cx
cmpxchg8b  qword ptr [esi + edi]
cmpxchg8b  qword ptr [esi]
cpuid
crc32  ecx, byte ptr [esi + edi]
crc32  ecx, byte ptr [esi]
crc32  ecx, dword ptr [esi + edi]
crc32  ecx, dword ptr [esi]
crc32  ecx, edx
cwd
cwde
daa
das
dec  byte ptr [esi + edi]
dec  byte ptr [esi]
dec  cl
imul  byte ptr [esi + edi]
imul  byte ptr [esi]
imul  cl
imul  cx
imul  cx, dx
imul  cx, dx, 0xa
imul  cx, word ptr [esi + edi]
imul  cx, word ptr [esi + edi], 0xa
imul  cx, word ptr [esi]
imul  cx, word ptr [esi], 0xa
imul  dword ptr [esi + edi]
imul  dword ptr [esi]
imul  ecx
imul  ecx, dword ptr [esi + edi]
imul  ecx, dword ptr [esi + edi], 0xa
imul  ecx, dword ptr [esi]
imul  ecx, dword ptr [esi], 0xa
imul  ecx, edx
imul  ecx, edx, 0xa
inc  byte ptr [esi + edi]
inc  byte ptr [esi]
inc  cl
lahf
lea  cx, [esi + edi]
lea  cx, [esi]
lock adc  byte ptr [esi + edi], 0xa
lock adc  byte ptr [esi + edi], cl
lock adc  byte ptr [esi], 0xa
lock adc  byte ptr [esi], cl
lock adc  dword ptr [esi + edi], 0xa
lock adc  dword ptr [esi + edi], ecx
lock adc  dword ptr [esi], 0xa
lock adc  dword ptr [esi], ecx
lock add  byte ptr [esi + edi], 0xa
lock add  byte ptr [esi + edi], cl
lock add  byte ptr [esi], 0xa
lock add  byte ptr [esi], cl
lock add  dword ptr [esi + edi], 0xa
lock add  dword ptr [esi + edi], ecx
lock add  dword ptr [esi], 0xa
lock add  dword ptr [esi], ecx
lock and  byte ptr [esi + edi], 0xa
lock and  byte ptr [esi + edi], cl
lock and  byte ptr [esi], 0xa
lock and  byte ptr [esi], cl
lock and  dword ptr [esi + edi], 0xa
lock and  dword ptr [esi + edi], ecx
lock and  dword ptr [esi], 0xa
lock and  dword ptr [esi], ecx
lock btc  dword ptr [esi + edi], 0xa
lock btc  dword ptr [esi + edi], ecx
lock btc  dword ptr [esi], 0xa
lock btc  dword ptr [esi], ecx
lock btr  dword ptr [esi + edi], 0xa
lock btr  dword ptr [esi + edi], ecx
lock btr  dword ptr [esi], 0xa
lock btr  dword ptr [esi], ecx
lock bts  dword ptr [esi + edi], 0xa
lock bts  dword ptr [esi + edi], ecx
lock bts  dword ptr [esi], 0xa
lock bts  dword ptr [esi], ecx
lock cmpxchg  byte ptr [esi + edi], cl
lock cmpxchg  byte ptr [esi], cl
lock cmpxchg  dword ptr [esi + edi], ecx
lock cmpxchg  dword ptr [esi], ecx
lock cmpxchg8b  qword ptr [esi + edi]
lock cmpxchg8b  qword ptr [esi]
lock dec  byte ptr [esi + edi]
lock dec  byte ptr [esi]
lock dec  dword ptr [esi + edi]
lock dec  dword ptr [esi]
lock inc  byte ptr [esi + edi]
lock inc  byte ptr [esi]
lock inc  dword ptr [esi + edi]
lock inc  dword ptr [esi]
lock neg  byte ptr [esi + edi]
lock neg  byte ptr [esi]
lock neg  dword ptr [esi + edi]
lock neg  dword ptr [esi]
lock not  byte ptr [esi + edi]
lock not  byte ptr [esi]
lock not  dword ptr [esi + edi]
lock not  dword ptr [esi]
lock or  byte ptr [esi + edi], 0xa
lock or  byte ptr [esi + edi], cl
lock or  byte ptr [esi], 0xa
lock or  byte ptr [esi], cl
lock or  dword ptr [esi + edi], 0xa
lock or  dword ptr [esi + edi], ecx
lock or  dword ptr [esi], 0xa
lock or  dword ptr [esi], ecx
lock sbb  byte ptr [esi + edi], 0xa
lock sbb  byte ptr [esi + edi], cl
lock sbb  byte ptr [esi], 0xa
lock sbb  byte ptr [esi], cl
lock sbb  dword ptr [esi + edi], 0xa
lock sbb  dword ptr [esi + edi], ecx
lock sbb  dword ptr [esi], 0xa
lock sbb  dword ptr [esi], ecx
lock sub  byte ptr [esi + edi], 0xa
lock sub  byte ptr [esi + edi], cl
lock sub  byte ptr [esi], 0xa
lock sub  byte ptr [esi], cl
lock sub  dword ptr [esi + edi], 0xa
lock sub  dword ptr [esi + edi], ecx
lock sub  dword ptr [esi], 0xa
lock sub  dword ptr [esi], ecx
lock xadd  byte ptr [esi + edi], cl
lock xadd  byte ptr [esi], cl
lock xadd  dword ptr [esi + edi], ecx
lock xadd  dword ptr [esi], ecx
lock xchg  byte ptr [esi + edi], cl
lock xchg  byte ptr [esi], cl
lock xchg  dword ptr [esi + edi], ecx
lock xchg  dword ptr [esi], ecx
lock xor  byte ptr [esi + edi], 0xa
lock xor  byte ptr [esi + edi], cl
lock xor  byte ptr [esi], 0xa
lock xor  byte ptr [esi], cl
lock xor  dword ptr [esi + edi], 0xa
lock xor  dword ptr [esi + edi], ecx
lock xor  dword ptr [esi], 0xa
lock xor  dword ptr [esi], ecx
lzcnt  ecx, dword ptr [esi + edi]
lzcnt  ecx, dword ptr [esi]
lzcnt  ecx, edx
mov  byte ptr [esi + edi], 0xa
mov  byte ptr [esi + edi], cl
mov  byte ptr [esi], 0xa
mov  byte ptr [esi], cl
mov  cl, byte ptr [esi + edi]
mov  cl, byte ptr [esi]
mov  cl, dl
mov  cx, 0xa
mov  cx, dx
mov  cx, word ptr [esi + edi]
mov  cx, word ptr [esi]
mov  word ptr [esi + edi], cx
mov  word ptr [esi], cx
movbe  cx, word ptr [esi + edi]
movbe  cx, word ptr [esi]
movbe  dword ptr [esi + edi], ecx
movbe  dword ptr [esi], ecx
movbe  ecx, dword ptr [esi + edi]
movbe  ecx, dword ptr [esi]
movbe  word ptr [esi + edi], cx
movbe  word ptr [esi], cx
movsx  cx, byte ptr [esi + edi]
movsx  cx, byte ptr [esi]
movsx  cx, dl
movsx  ecx, byte ptr [esi + edi]
movsx  ecx, byte ptr [esi]
movsx  ecx, word ptr [esi + edi]
movsx  ecx, word ptr [esi]
movzx  cx, byte ptr [esi + edi]
movzx  cx, byte ptr [esi]
movzx  cx, dl
movzx  ecx, byte ptr [esi + edi]
movzx  ecx, byte ptr [esi]
movzx  ecx, word ptr [esi + edi]
movzx  ecx, word ptr [esi]
mul  byte ptr [esi + edi]
mul  byte ptr [esi]
mul  cl
mul  cx
mul  dword ptr [esi + edi]
mul  dword ptr [esi]
mul  ecx
neg  byte ptr [esi + edi]
neg  byte ptr [esi]
neg  cl
neg  cx
not  byte ptr [esi + edi]
not  byte ptr [esi]
not  cl
not  cx
or  byte ptr [esi + edi], 0xa
or  byte ptr [esi + edi], cl
or  byte ptr [esi], 0xa
or  byte ptr [esi], cl
or  cl, 0xa
or  cl, byte ptr [esi + edi]
or  cl, byte ptr [esi]
or  cl, dl
or  cx, 0xa
or  cx, dx
or  cx, word ptr [esi + edi]
or  cx, word ptr [esi]
or  word ptr [esi + edi], cx
or  word ptr [esi], cx
pause
popcnt  ecx, dword ptr [esi + edi]
popcnt  ecx, dword ptr [esi]
popcnt  ecx, edx
rcl  byte ptr [esi + edi], 0xa
rcl  byte ptr [esi + edi], 1
rcl  byte ptr [esi + edi], cl
rcl  byte ptr [esi], 0xa
rcl  byte ptr [esi], 1
rcl  byte ptr [esi], cl
rcl  cl, 0xa
rcl  cl, 1
rcl  cx, 0xa
rcl  cx, 1
rcl  dword ptr [esi + edi], 0xa
rcl  dword ptr [esi + edi], 1
rcl  dword ptr [esi + edi], cl
rcl  dword ptr [esi], 0xa
rcl  dword ptr [esi], 1
rcl  dword ptr [esi], cl
rcl  ecx, 0xa
rcl  ecx, 1
rcr  byte ptr [esi + edi], 0xa
rcr  byte ptr [esi + edi], 1
rcr  byte ptr [esi + edi], cl
rcr  byte ptr [esi], 0xa
rcr  byte ptr [esi], 1
rcr  byte ptr [esi], cl
rcr  cl, 0xa
rcr  cl, 1
rcr  cx, 0xa
rcr  cx, 1
rcr  dword ptr [esi + edi], 0xa
rcr  dword ptr [esi + edi], 1
rcr  dword ptr [esi + edi], cl
rcr  dword ptr [esi], 0xa
rcr  dword ptr [esi], 1
rcr  dword ptr [esi], cl
rcr  ecx, 0xa
rcr  ecx, 1
rdrand  cx
rdrand  ecx
rdseed  cx
rdseed  ecx
rdtsc
rdtscp
rol  byte ptr [esi + edi], 0xa
rol  byte ptr [esi + edi], 1
rol  byte ptr [esi + edi], cl
rol  byte ptr [esi], 0xa
rol  byte ptr [esi], 1
rol  byte ptr [esi], cl
rol  cl, 0xa
rol  cl, 1
rol  cx, 0xa
rol  cx, 1
rol  dword ptr [esi + edi], 0xa
rol  dword ptr [esi + edi], 1
rol  dword ptr [esi + edi], cl
rol  dword ptr [esi], 0xa
rol  dword ptr [esi], 1
rol  dword ptr [esi], cl
rol  ecx, 0xa
rol  ecx, 1
ror  byte ptr [esi + edi], 0xa
ror  byte ptr [esi + edi], 1
ror  byte ptr [esi + edi], cl
ror  byte ptr [esi], 0xa
ror  byte ptr [esi], 1
ror  byte ptr [esi], cl
ror  cl, 0xa
ror  cl, 1
ror  cx, 0xa
ror  cx, 1
ror  dword ptr [esi + edi], cl
ror  dword ptr [esi], cl
sal  byte ptr [esi + edi], 0xa
sal  byte ptr [esi + edi], 1
sal  byte ptr [esi + edi], cl
sal  byte ptr [esi], 0xa
sal  byte ptr [esi], 1
sal  byte ptr [esi], cl
sal  cl, 0xa
sal  cl, 1
sal  cx, 0xa
sal  cx, 1
sal  dword ptr [esi + edi], cl
sal  dword ptr [esi], cl
sar  byte ptr [esi + edi], 0xa
sar  byte ptr [esi + edi], 1
sar  byte ptr [esi + edi], cl
sar  byte ptr [esi], 0xa
sar  byte ptr [esi], 1
sar  byte ptr [esi], cl
sar  cl, 0xa
sar  cl, 1
sar  cx, 0xa
sar  cx, 1
sar  dword ptr [esi + edi], cl
sar  dword ptr [esi], cl
sbb  byte ptr [esi + edi], 0xa
sbb  byte ptr [esi + edi], cl
sbb  byte ptr [esi], 0xa
sbb  byte ptr [esi], cl
sbb  cl, 0xa
sbb  cl, byte ptr [esi + edi]
sbb  cl, byte ptr [esi]
sbb  cl, dl
sbb  cx, 0xa
sbb  cx, dx
sbb  cx, word ptr [esi + edi]
sbb  cx, word ptr [esi]
sbb  word ptr [esi + edi], cx
sbb  word ptr [esi], cx
seta  byte ptr [esi + edi]
seta  byte ptr [esi]
setae  byte ptr [esi + edi]
setae  byte ptr [esi]
setb  byte ptr [esi + edi]
setb  byte ptr [esi]
setbe  byte ptr [esi + edi]
setbe  byte ptr [esi]
sete  byte ptr [esi + edi]
sete  byte ptr [esi]
setg  byte ptr [esi + edi]
setg  byte ptr [esi]
setge  byte ptr [esi + edi]
setge  byte ptr [esi]
setl  byte ptr [esi + edi]
setl  byte ptr [esi]
setle  byte ptr [esi + edi]
setle  byte ptr [esi]
setne  byte ptr [esi + edi]
setne  byte ptr [esi]
setno  byte ptr [esi + edi]
setno  byte ptr [esi]
setnp  byte ptr [esi + edi]
setnp  byte ptr [esi]
setns  byte ptr [esi + edi]
setns  byte ptr [esi]
seto  byte ptr [esi + edi]
seto  byte ptr [esi]
setp  byte ptr [esi + edi]
setp  byte ptr [esi]
sets  byte ptr [esi + edi]
sets  byte ptr [esi]
shl  byte ptr [esi + edi], 0xa
shl  byte ptr [esi + edi], 1
shl  byte ptr [esi + edi], cl
shl  byte ptr [esi], 0xa
shl  byte ptr [esi], 1
shl  byte ptr [esi], cl
shl  cl, 0xa
shl  cl, 1
shl  cx, 0xa
shl  cx, 1
shl  dword ptr [esi + edi], cl
shl  dword ptr [esi], cl
shld  cx, dx, 0xa
shld  cx, dx, cl
shld  dword ptr [esi + edi], ecx, 0xa
shld  dword ptr [esi], ecx, 0xa
shld  ecx, edx, 0xa
shld  ecx, edx, cl
shld  word ptr [esi + edi], cx, 0xa
shld  word ptr [esi], cx, 0xa
shr  byte ptr [esi + edi], 0xa
shr  byte ptr [esi + edi], 1
shr  byte ptr [esi + edi], cl
shr  byte ptr [esi], 0xa
shr  byte ptr [esi], 1
shr  byte ptr [esi], cl
shr  cl, 0xa
shr  cl, 1
shr  cx, 0xa
shr  cx, 1
shr  dword ptr [esi + edi], cl
shr  dword ptr [esi], cl
shrd  cx, dx, 0xa
shrd  cx, dx, cl
shrd  dword ptr [esi + edi], ecx, 0xa
shrd  dword ptr [esi], ecx, 0xa
shrd  ecx, edx, 0xa
shrd  ecx, edx, cl
shrd  word ptr [esi + edi], cx, 0xa
shrd  word ptr [esi], cx, 0xa
smsw  cx
smsw  ecx
smsw  word ptr [esi + edi]
smsw  word ptr [esi]
sub  byte ptr [esi + edi], 0xa
sub  byte ptr [esi + edi], cl
sub  byte ptr [esi], 0xa
sub  byte ptr [esi], cl
sub  cl, 0xa
sub  cl, byte ptr [esi + edi]
sub  cl, byte ptr [esi]
sub  cl, dl
sub  cx, 0xa
sub  cx, dx
sub  cx, word ptr [esi + edi]
sub  cx, word ptr [esi]
sub  word ptr [esi + edi], cx
sub  word ptr [esi], cx
test  byte ptr [esi + edi], 0xa
test  byte ptr [esi + edi], cl
test  byte ptr [esi], 0xa
test  byte ptr [esi], cl
test  cl, 0xa
test  cx, 0xa
test  word ptr [esi + edi], cx
test  word ptr [esi], cx
tzcnt  ecx, dword ptr [esi + edi]
tzcnt  ecx, dword ptr [esi]
tzcnt  ecx, edx
xadd  byte ptr [esi + edi], cl
xadd  byte ptr [esi], cl
xadd  cl, dl
xadd  cx, dx
xadd  dword ptr [esi + edi], ecx
xadd  dword ptr [esi], ecx
xadd  ecx, edx
xadd  word ptr [esi + edi], cx
xadd  word ptr [esi], cx
xchg  byte ptr [esi + edi], cl
xchg  byte ptr [esi], cl
xchg  cl, dl
xchg  cx, dx
xchg  word ptr [esi + edi], cx
xchg  word ptr [esi], cx
xor  byte ptr [esi + edi], 0xa
xor  byte ptr [esi + edi], cl
xor  byte ptr [esi], 0xa
xor  byte ptr [esi], cl
xor  cl, 0xa
xor  cl, byte ptr [esi + edi]
xor  cl, byte ptr [esi]
xor  cl, dl
xor  cx, 0xa
xor  cx, dx
xor  cx, word ptr [esi + edi]
xor  cx, word ptr [esi]
xor  word ptr [esi + edi], cx
xor  word ptr [esi], cx
```


### x87
```assembly
f2xm1
fabs
fadd  dword ptr [esi + edi]
fadd  dword ptr [esi]
fadd  qword ptr [esi + edi]
fadd  qword ptr [esi]
fadd  st(0)
fadd  st(0), st(0)
faddp  st(0)
fbld  tbyte ptr [esi + edi]
fbld  tbyte ptr [esi]
fbstp  tbyte ptr [esi + edi]
fbstp  tbyte ptr [esi]
fchs
fcmovb  st(0), st(0)
fcmovbe  st(0), st(0)
fcmove  st(0), st(0)
fcmovnb  st(0), st(0)
fcmovnbe  st(0), st(0)
fcmovne  st(0), st(0)
fcmovnu  st(0), st(0)
fcmovu  st(0), st(0)
fcom  dword ptr [esi + edi]
fcom  dword ptr [esi]
fcom  qword ptr [esi + edi]
fcom  qword ptr [esi]
fcom  st(0)
fcomi  st(0)
fcomip  st(0)
fcomp  dword ptr [esi + edi]
fcomp  dword ptr [esi]
fcomp  qword ptr [esi + edi]
fcomp  qword ptr [esi]
fcomp  st(0)
fcompp
fcos
fdecstp
fdiv  dword ptr [esi + edi]
fdiv  dword ptr [esi]
fdiv  qword ptr [esi + edi]
fdiv  qword ptr [esi]
fdiv  st(0)
fdiv  st(0), st(0)
fdivp  st(0)
fdivr  dword ptr [esi + edi]
fdivr  dword ptr [esi]
fdivr  qword ptr [esi + edi]
fdivr  qword ptr [esi]
fdivr  st(0)
fdivr  st(0), st(0)
fdivrp  st(0)
ffree  st(0)
ffreep  st(0)
fiadd  dword ptr [esi + edi]
fiadd  dword ptr [esi]
fiadd  word ptr [esi + edi]
fiadd  word ptr [esi]
ficom  dword ptr [esi + edi]
ficom  dword ptr [esi]
ficom  word ptr [esi + edi]
ficom  word ptr [esi]
ficomp  dword ptr [esi + edi]
ficomp  dword ptr [esi]
ficomp  word ptr [esi + edi]
ficomp  word ptr [esi]
fidiv  dword ptr [esi + edi]
fidiv  dword ptr [esi]
fidiv  word ptr [esi + edi]
fidiv  word ptr [esi]
fidivr  dword ptr [esi + edi]
fidivr  dword ptr [esi]
fidivr  word ptr [esi + edi]
fidivr  word ptr [esi]
fild  dword ptr [esi + edi]
fild  dword ptr [esi]
fild  qword ptr [esi + edi]
fild  qword ptr [esi]
fild  word ptr [esi + edi]
fild  word ptr [esi]
fimul  dword ptr [esi + edi]
fimul  dword ptr [esi]
fimul  word ptr [esi + edi]
fimul  word ptr [esi]
fincstp
fist  dword ptr [esi + edi]
fist  dword ptr [esi]
fist  word ptr [esi + edi]
fist  word ptr [esi]
fistp  dword ptr [esi + edi]
fistp  dword ptr [esi]
fistp  qword ptr [esi + edi]
fistp  qword ptr [esi]
fistp  word ptr [esi + edi]
fistp  word ptr [esi]
fisub  dword ptr [esi + edi]
fisub  dword ptr [esi]
fisub  word ptr [esi + edi]
fisub  word ptr [esi]
fisubr  dword ptr [esi + edi]
fisubr  dword ptr [esi]
fisubr  word ptr [esi + edi]
fisubr  word ptr [esi]
fld  dword ptr [esi + edi]
fld  dword ptr [esi]
fld  qword ptr [esi + edi]
fld  qword ptr [esi]
fld  st(0)
fld  tbyte ptr [esi + edi]
fld  tbyte ptr [esi]
fld1
fldcw  word ptr [esi + edi]
fldcw  word ptr [esi]
fldenv  [esi + edi]
fldenv  [esi]
fldl2e
fldl2t
fldlg2
fldln2
fldpi
fldz
fmul  dword ptr [esi + edi]
fmul  dword ptr [esi]
fmul  qword ptr [esi + edi]
fmul  qword ptr [esi]
fmul  st(0)
fmul  st(0), st(0)
fmulp  st(0)
fnclex
fninit
fnop
fnsave  [esi + edi]
fnsave  [esi]
fnstcw  word ptr [esi + edi]
fnstcw  word ptr [esi]
fnstenv  [esi + edi]
fnstenv  [esi]
fnstsw  ax
fnstsw  word ptr [esi + edi]
fnstsw  word ptr [esi]
fpatan
fprem
fprem1
fptan
frndint
frstor  [esi + edi]
frstor  [esi]
fscale
fsetpm
fsin
fsincos
fsqrt
fst  dword ptr [esi + edi]
fst  dword ptr [esi]
fst  qword ptr [esi + edi]
fst  qword ptr [esi]
fst  st(0)
fstp  dword ptr [esi + edi]
fstp  dword ptr [esi]
fstp  qword ptr [esi + edi]
fstp  qword ptr [esi]
fstp  st(0)
fstp  tbyte ptr [esi + edi]
fstp  tbyte ptr [esi]
fsub  dword ptr [esi + edi]
fsub  dword ptr [esi]
fsub  qword ptr [esi + edi]
fsub  qword ptr [esi]
fsub  st(0)
fsub  st(0), st(0)
fsubp  st(0)
fsubr  dword ptr [esi + edi]
fsubr  dword ptr [esi]
fsubr  qword ptr [esi + edi]
fsubr  qword ptr [esi]
fsubr  st(0)
fsubr  st(0), st(0)
fsubrp  st(0)
ftst
fucom  st(0)
fucomi  st(0)
fucomip  st(0)
fucomp  st(0)
fucompp
fxam
fxch  st(0)
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
fxtract
fyl2x
fyl2xp1
wait
```


### sse/sse2
```assembly
addpd  xmm0, xmm1
addpd  xmm0, xmmword ptr [esi + edi]
addpd  xmm0, xmmword ptr [esi]
addps  xmm0, xmm1
addps  xmm0, xmmword ptr [esi + edi]
addps  xmm0, xmmword ptr [esi]
addsd  xmm0, qword ptr [esi + edi]
addsd  xmm0, qword ptr [esi]
addsd  xmm0, xmm1
addss  xmm0, dword ptr [esi + edi]
addss  xmm0, dword ptr [esi]
addss  xmm0, xmm1
andnpd  xmm0, xmm1
andnpd  xmm0, xmmword ptr [esi + edi]
andnpd  xmm0, xmmword ptr [esi]
andnps  xmm0, xmm1
andnps  xmm0, xmmword ptr [esi + edi]
andnps  xmm0, xmmword ptr [esi]
andpd  xmm0, xmm1
andpd  xmm0, xmmword ptr [esi + edi]
andpd  xmm0, xmmword ptr [esi]
andps  xmm0, xmm1
andps  xmm0, xmmword ptr [esi + edi]
andps  xmm0, xmmword ptr [esi]
cmppd  xmm0, xmm1, 0xa
cmppd  xmm0, xmmword ptr [esi + edi], 0xa
cmppd  xmm0, xmmword ptr [esi], 0xa
cmpps  xmm0, xmm1, 0xa
cmpps  xmm0, xmmword ptr [esi + edi], 0xa
cmpps  xmm0, xmmword ptr [esi], 0xa
cmpsd  xmm0, qword ptr [esi + edi], 0xa
cmpsd  xmm0, qword ptr [esi], 0xa
cmpsd  xmm0, xmm1, 0xa
cmpss  xmm0, dword ptr [esi + edi], 0xa
cmpss  xmm0, dword ptr [esi], 0xa
cmpss  xmm0, xmm1, 0xa
comisd  xmm0, qword ptr [esi + edi]
comisd  xmm0, qword ptr [esi]
comisd  xmm0, xmm1
comiss  xmm0, dword ptr [esi + edi]
comiss  xmm0, dword ptr [esi]
comiss  xmm0, xmm1
cvtdq2pd  xmm0, qword ptr [esi + edi]
cvtdq2pd  xmm0, qword ptr [esi]
cvtdq2pd  xmm0, xmm1
cvtdq2ps  xmm0, xmm1
cvtdq2ps  xmm0, xmmword ptr [esi + edi]
cvtdq2ps  xmm0, xmmword ptr [esi]
cvtpd2dq  xmm0, xmm1
cvtpd2dq  xmm0, xmmword ptr [esi + edi]
cvtpd2dq  xmm0, xmmword ptr [esi]
cvtpd2ps  xmm0, xmm1
cvtpd2ps  xmm0, xmmword ptr [esi + edi]
cvtpd2ps  xmm0, xmmword ptr [esi]
cvtpi2pd  xmm0, qword ptr [esi + edi]
cvtpi2pd  xmm0, qword ptr [esi]
cvtpi2ps  xmm0, qword ptr [esi + edi]
cvtpi2ps  xmm0, qword ptr [esi]
cvtps2dq  xmm0, xmm1
cvtps2dq  xmm0, xmmword ptr [esi + edi]
cvtps2dq  xmm0, xmmword ptr [esi]
cvtps2pd  xmm0, qword ptr [esi + edi]
cvtps2pd  xmm0, qword ptr [esi]
cvtps2pd  xmm0, xmm1
cvtsd2si  ecx, qword ptr [esi + edi]
cvtsd2si  ecx, qword ptr [esi]
cvtsd2si  ecx, xmm0
cvtsd2ss  xmm0, qword ptr [esi + edi]
cvtsd2ss  xmm0, qword ptr [esi]
cvtsd2ss  xmm0, xmm1
cvtsi2sd  xmm0, dword ptr [esi + edi]
cvtsi2sd  xmm0, dword ptr [esi]
cvtsi2sd  xmm0, ecx
cvtsi2ss  xmm0, dword ptr [esi + edi]
cvtsi2ss  xmm0, dword ptr [esi]
cvtsi2ss  xmm0, ecx
cvtss2sd  xmm0, dword ptr [esi + edi]
cvtss2sd  xmm0, dword ptr [esi]
cvtss2sd  xmm0, xmm1
cvtss2si  ecx, dword ptr [esi + edi]
cvtss2si  ecx, dword ptr [esi]
cvtss2si  ecx, xmm0
cvttpd2dq  xmm0, xmm1
cvttpd2dq  xmm0, xmmword ptr [esi + edi]
cvttpd2dq  xmm0, xmmword ptr [esi]
cvttps2dq  xmm0, xmm1
cvttps2dq  xmm0, xmmword ptr [esi + edi]
cvttps2dq  xmm0, xmmword ptr [esi]
cvttsd2si  ecx, qword ptr [esi + edi]
cvttsd2si  ecx, qword ptr [esi]
cvttsd2si  ecx, xmm0
cvttss2si  ecx, dword ptr [esi + edi]
cvttss2si  ecx, dword ptr [esi]
cvttss2si  ecx, xmm0
divpd  xmm0, xmm1
divpd  xmm0, xmmword ptr [esi + edi]
divpd  xmm0, xmmword ptr [esi]
divps  xmm0, xmm1
divps  xmm0, xmmword ptr [esi + edi]
divps  xmm0, xmmword ptr [esi]
divsd  xmm0, qword ptr [esi + edi]
divsd  xmm0, qword ptr [esi]
divsd  xmm0, xmm1
divss  xmm0, dword ptr [esi + edi]
divss  xmm0, dword ptr [esi]
divss  xmm0, xmm1
fxrstor  [esi + edi]
fxrstor  [esi]
fxsave  [esi + edi]
fxsave  [esi]
ldmxcsr  dword ptr [esi + edi]
ldmxcsr  dword ptr [esi]
lfence
maskmovdqu  xmm0, xmm1
maxpd  xmm0, xmm1
maxpd  xmm0, xmmword ptr [esi + edi]
maxpd  xmm0, xmmword ptr [esi]
maxps  xmm0, xmm1
maxps  xmm0, xmmword ptr [esi + edi]
maxps  xmm0, xmmword ptr [esi]
maxsd  xmm0, qword ptr [esi + edi]
maxsd  xmm0, qword ptr [esi]
maxsd  xmm0, xmm1
maxss  xmm0, dword ptr [esi + edi]
maxss  xmm0, dword ptr [esi]
maxss  xmm0, xmm1
mfence
minpd  xmm0, xmm1
minpd  xmm0, xmmword ptr [esi + edi]
minpd  xmm0, xmmword ptr [esi]
minps  xmm0, xmm1
minps  xmm0, xmmword ptr [esi + edi]
minps  xmm0, xmmword ptr [esi]
minsd  xmm0, qword ptr [esi + edi]
minsd  xmm0, qword ptr [esi]
minsd  xmm0, xmm1
minss  xmm0, dword ptr [esi + edi]
minss  xmm0, dword ptr [esi]
minss  xmm0, xmm1
movapd  xmm0, xmm1
movapd  xmm0, xmmword ptr [esi + edi]
movapd  xmm0, xmmword ptr [esi]
movapd  xmmword ptr [esi + edi], xmm0
movapd  xmmword ptr [esi], xmm0
movaps  xmm0, xmm1
movaps  xmm0, xmmword ptr [esi + edi]
movaps  xmm0, xmmword ptr [esi]
movaps  xmmword ptr [esi + edi], xmm0
movaps  xmmword ptr [esi], xmm0
movd  dword ptr [esi + edi], xmm0
movd  dword ptr [esi], xmm0
movd  ecx, xmm0
movd  xmm0, dword ptr [esi + edi]
movd  xmm0, dword ptr [esi]
movd  xmm0, ecx
movdqa  xmm0, xmm1
movdqa  xmm0, xmmword ptr [esi + edi]
movdqa  xmm0, xmmword ptr [esi]
movdqa  xmmword ptr [esi + edi], xmm0
movdqa  xmmword ptr [esi], xmm0
movdqu  xmm0, xmm1
movdqu  xmm0, xmmword ptr [esi + edi]
movdqu  xmm0, xmmword ptr [esi]
movdqu  xmmword ptr [esi + edi], xmm0
movdqu  xmmword ptr [esi], xmm0
movhlps  xmm0, xmm1
movhpd  qword ptr [esi + edi], xmm0
movhpd  qword ptr [esi], xmm0
movhpd  xmm0, qword ptr [esi + edi]
movhpd  xmm0, qword ptr [esi]
movhps  qword ptr [esi + edi], xmm0
movhps  qword ptr [esi], xmm0
movhps  xmm0, qword ptr [esi + edi]
movhps  xmm0, qword ptr [esi]
movlhps  xmm0, xmm1
movlpd  qword ptr [esi + edi], xmm0
movlpd  qword ptr [esi], xmm0
movlpd  xmm0, qword ptr [esi + edi]
movlpd  xmm0, qword ptr [esi]
movlps  qword ptr [esi + edi], xmm0
movlps  qword ptr [esi], xmm0
movlps  xmm0, qword ptr [esi + edi]
movlps  xmm0, qword ptr [esi]
movmskpd  ecx, xmm0
movmskps  ecx, xmm0
movntdq  xmmword ptr [esi + edi], xmm0
movntdq  xmmword ptr [esi], xmm0
movnti  dword ptr [esi + edi], ecx
movnti  dword ptr [esi], ecx
movntpd  xmmword ptr [esi + edi], xmm0
movntpd  xmmword ptr [esi], xmm0
movntps  xmmword ptr [esi + edi], xmm0
movntps  xmmword ptr [esi], xmm0
movq  qword ptr [esi + edi], xmm0
movq  qword ptr [esi], xmm0
movq  xmm0, qword ptr [esi + edi]
movq  xmm0, qword ptr [esi]
movq  xmm0, xmm1
movsd  qword ptr [esi + edi], xmm0
movsd  qword ptr [esi], xmm0
movsd  xmm0, qword ptr [esi + edi]
movsd  xmm0, qword ptr [esi]
movsd  xmm0, xmm1
movss  dword ptr [esi + edi], xmm0
movss  dword ptr [esi], xmm0
movss  xmm0, dword ptr [esi + edi]
movss  xmm0, dword ptr [esi]
movss  xmm0, xmm1
movupd  xmm0, xmm1
movupd  xmm0, xmmword ptr [esi + edi]
movupd  xmm0, xmmword ptr [esi]
movupd  xmmword ptr [esi + edi], xmm0
movupd  xmmword ptr [esi], xmm0
movups  xmm0, xmm1
movups  xmm0, xmmword ptr [esi + edi]
movups  xmm0, xmmword ptr [esi]
movups  xmmword ptr [esi + edi], xmm0
movups  xmmword ptr [esi], xmm0
mulpd  xmm0, xmm1
mulpd  xmm0, xmmword ptr [esi + edi]
mulpd  xmm0, xmmword ptr [esi]
mulps  xmm0, xmm1
mulps  xmm0, xmmword ptr [esi + edi]
mulps  xmm0, xmmword ptr [esi]
mulsd  xmm0, qword ptr [esi + edi]
mulsd  xmm0, qword ptr [esi]
mulsd  xmm0, xmm1
mulss  xmm0, dword ptr [esi + edi]
mulss  xmm0, dword ptr [esi]
mulss  xmm0, xmm1
orpd  xmm0, xmm1
orpd  xmm0, xmmword ptr [esi + edi]
orpd  xmm0, xmmword ptr [esi]
orps  xmm0, xmm1
orps  xmm0, xmmword ptr [esi + edi]
orps  xmm0, xmmword ptr [esi]
packssdw  xmm0, xmm1
packssdw  xmm0, xmmword ptr [esi + edi]
packssdw  xmm0, xmmword ptr [esi]
packsswb  xmm0, xmm1
packsswb  xmm0, xmmword ptr [esi + edi]
packsswb  xmm0, xmmword ptr [esi]
packuswb  xmm0, xmm1
packuswb  xmm0, xmmword ptr [esi + edi]
packuswb  xmm0, xmmword ptr [esi]
paddb  xmm0, xmm1
paddb  xmm0, xmmword ptr [esi + edi]
paddb  xmm0, xmmword ptr [esi]
paddd  xmm0, xmm1
paddd  xmm0, xmmword ptr [esi + edi]
paddd  xmm0, xmmword ptr [esi]
paddq  xmm0, xmm1
paddq  xmm0, xmmword ptr [esi + edi]
paddq  xmm0, xmmword ptr [esi]
paddsb  xmm0, xmm1
paddsb  xmm0, xmmword ptr [esi + edi]
paddsb  xmm0, xmmword ptr [esi]
paddsw  xmm0, xmm1
paddsw  xmm0, xmmword ptr [esi + edi]
paddsw  xmm0, xmmword ptr [esi]
paddusb  xmm0, xmm1
paddusb  xmm0, xmmword ptr [esi + edi]
paddusb  xmm0, xmmword ptr [esi]
paddusw  xmm0, xmm1
paddusw  xmm0, xmmword ptr [esi + edi]
paddusw  xmm0, xmmword ptr [esi]
paddw  xmm0, xmm1
paddw  xmm0, xmmword ptr [esi + edi]
paddw  xmm0, xmmword ptr [esi]
pand  xmm0, xmm1
pand  xmm0, xmmword ptr [esi + edi]
pand  xmm0, xmmword ptr [esi]
pandn  xmm0, xmm1
pandn  xmm0, xmmword ptr [esi + edi]
pandn  xmm0, xmmword ptr [esi]
pavgb  xmm0, xmm1
pavgb  xmm0, xmmword ptr [esi + edi]
pavgb  xmm0, xmmword ptr [esi]
pavgw  xmm0, xmm1
pavgw  xmm0, xmmword ptr [esi + edi]
pavgw  xmm0, xmmword ptr [esi]
pcmpeqb  xmm0, xmm1
pcmpeqb  xmm0, xmmword ptr [esi + edi]
pcmpeqb  xmm0, xmmword ptr [esi]
pcmpeqd  xmm0, xmm1
pcmpeqd  xmm0, xmmword ptr [esi + edi]
pcmpeqd  xmm0, xmmword ptr [esi]
pcmpeqw  xmm0, xmm1
pcmpeqw  xmm0, xmmword ptr [esi + edi]
pcmpeqw  xmm0, xmmword ptr [esi]
pcmpgtb  xmm0, xmm1
pcmpgtb  xmm0, xmmword ptr [esi + edi]
pcmpgtb  xmm0, xmmword ptr [esi]
pcmpgtd  xmm0, xmm1
pcmpgtd  xmm0, xmmword ptr [esi + edi]
pcmpgtd  xmm0, xmmword ptr [esi]
pcmpgtw  xmm0, xmm1
pcmpgtw  xmm0, xmmword ptr [esi + edi]
pcmpgtw  xmm0, xmmword ptr [esi]
pextrw  ecx, xmm0, 0xa
pinsrw  xmm0, ecx, 0xa
pinsrw  xmm0, word ptr [esi + edi], 0xa
pinsrw  xmm0, word ptr [esi], 0xa
pmaddwd  xmm0, xmm1
pmaddwd  xmm0, xmmword ptr [esi + edi]
pmaddwd  xmm0, xmmword ptr [esi]
pmaxsw  xmm0, xmm1
pmaxsw  xmm0, xmmword ptr [esi + edi]
pmaxsw  xmm0, xmmword ptr [esi]
pmaxub  xmm0, xmm1
pmaxub  xmm0, xmmword ptr [esi + edi]
pmaxub  xmm0, xmmword ptr [esi]
pminsw  xmm0, xmm1
pminsw  xmm0, xmmword ptr [esi + edi]
pminsw  xmm0, xmmword ptr [esi]
pminub  xmm0, xmm1
pminub  xmm0, xmmword ptr [esi + edi]
pminub  xmm0, xmmword ptr [esi]
pmovmskb  ecx, xmm0
pmulhuw  xmm0, xmm1
pmulhuw  xmm0, xmmword ptr [esi + edi]
pmulhuw  xmm0, xmmword ptr [esi]
pmulhw  xmm0, xmm1
pmulhw  xmm0, xmmword ptr [esi + edi]
pmulhw  xmm0, xmmword ptr [esi]
pmullw  xmm0, xmm1
pmullw  xmm0, xmmword ptr [esi + edi]
pmullw  xmm0, xmmword ptr [esi]
pmuludq  xmm0, xmm1
pmuludq  xmm0, xmmword ptr [esi + edi]
pmuludq  xmm0, xmmword ptr [esi]
por  xmm0, xmm1
por  xmm0, xmmword ptr [esi + edi]
por  xmm0, xmmword ptr [esi]
prefetchnta  byte ptr [esi + edi]
prefetchnta  byte ptr [esi]
prefetcht0  byte ptr [esi + edi]
prefetcht0  byte ptr [esi]
prefetcht1  byte ptr [esi + edi]
prefetcht1  byte ptr [esi]
prefetcht2  byte ptr [esi + edi]
prefetcht2  byte ptr [esi]
psadbw  xmm0, xmm1
psadbw  xmm0, xmmword ptr [esi + edi]
psadbw  xmm0, xmmword ptr [esi]
pshufd  xmm0, xmm1, 0xa
pshufd  xmm0, xmmword ptr [esi + edi], 0xa
pshufd  xmm0, xmmword ptr [esi], 0xa
pshufhw  xmm0, xmm1, 0xa
pshufhw  xmm0, xmmword ptr [esi + edi], 0xa
pshufhw  xmm0, xmmword ptr [esi], 0xa
pshuflw  xmm0, xmm1, 0xa
pshuflw  xmm0, xmmword ptr [esi + edi], 0xa
pshuflw  xmm0, xmmword ptr [esi], 0xa
pslld  xmm0, 0xa
pslld  xmm0, xmm1
pslld  xmm0, xmmword ptr [esi + edi]
pslld  xmm0, xmmword ptr [esi]
pslldq  xmm0, 0xa
psllq  xmm0, 0xa
psllq  xmm0, xmm1
psllq  xmm0, xmmword ptr [esi + edi]
psllq  xmm0, xmmword ptr [esi]
psllw  xmm0, 0xa
psllw  xmm0, xmm1
psllw  xmm0, xmmword ptr [esi + edi]
psllw  xmm0, xmmword ptr [esi]
psrad  xmm0, 0xa
psrad  xmm0, xmm1
psrad  xmm0, xmmword ptr [esi + edi]
psrad  xmm0, xmmword ptr [esi]
psraw  xmm0, 0xa
psraw  xmm0, xmm1
psraw  xmm0, xmmword ptr [esi + edi]
psraw  xmm0, xmmword ptr [esi]
psrld  xmm0, 0xa
psrld  xmm0, xmm1
psrld  xmm0, xmmword ptr [esi + edi]
psrld  xmm0, xmmword ptr [esi]
psrldq  xmm0, 0xa
psrlq  xmm0, 0xa
psrlq  xmm0, xmm1
psrlq  xmm0, xmmword ptr [esi + edi]
psrlq  xmm0, xmmword ptr [esi]
psrlw  xmm0, 0xa
psrlw  xmm0, xmm1
psrlw  xmm0, xmmword ptr [esi + edi]
psrlw  xmm0, xmmword ptr [esi]
psubb  xmm0, xmm1
psubb  xmm0, xmmword ptr [esi + edi]
psubb  xmm0, xmmword ptr [esi]
psubd  xmm0, xmm1
psubd  xmm0, xmmword ptr [esi + edi]
psubd  xmm0, xmmword ptr [esi]
psubq  xmm0, xmm1
psubq  xmm0, xmmword ptr [esi + edi]
psubq  xmm0, xmmword ptr [esi]
psubsb  xmm0, xmm1
psubsb  xmm0, xmmword ptr [esi + edi]
psubsb  xmm0, xmmword ptr [esi]
psubsw  xmm0, xmm1
psubsw  xmm0, xmmword ptr [esi + edi]
psubsw  xmm0, xmmword ptr [esi]
psubusb  xmm0, xmm1
psubusb  xmm0, xmmword ptr [esi + edi]
psubusb  xmm0, xmmword ptr [esi]
psubusw  xmm0, xmm1
psubusw  xmm0, xmmword ptr [esi + edi]
psubusw  xmm0, xmmword ptr [esi]
psubw  xmm0, xmm1
psubw  xmm0, xmmword ptr [esi + edi]
psubw  xmm0, xmmword ptr [esi]
punpckhbw  xmm0, xmm1
punpckhbw  xmm0, xmmword ptr [esi + edi]
punpckhbw  xmm0, xmmword ptr [esi]
punpckhdq  xmm0, xmm1
punpckhdq  xmm0, xmmword ptr [esi + edi]
punpckhdq  xmm0, xmmword ptr [esi]
punpckhqdq  xmm0, xmm1
punpckhqdq  xmm0, xmmword ptr [esi + edi]
punpckhqdq  xmm0, xmmword ptr [esi]
punpckhwd  xmm0, xmm1
punpckhwd  xmm0, xmmword ptr [esi + edi]
punpckhwd  xmm0, xmmword ptr [esi]
punpcklbw  xmm0, xmm1
punpcklbw  xmm0, xmmword ptr [esi + edi]
punpcklbw  xmm0, xmmword ptr [esi]
punpckldq  xmm0, xmm1
punpckldq  xmm0, xmmword ptr [esi + edi]
punpckldq  xmm0, xmmword ptr [esi]
punpcklqdq  xmm0, xmm1
punpcklqdq  xmm0, xmmword ptr [esi + edi]
punpcklqdq  xmm0, xmmword ptr [esi]
punpcklwd  xmm0, xmm1
punpcklwd  xmm0, xmmword ptr [esi + edi]
punpcklwd  xmm0, xmmword ptr [esi]
pxor  xmm0, xmm1
pxor  xmm0, xmmword ptr [esi + edi]
pxor  xmm0, xmmword ptr [esi]
rcpps  xmm0, xmm1
rcpps  xmm0, xmmword ptr [esi + edi]
rcpps  xmm0, xmmword ptr [esi]
rcpss  xmm0, dword ptr [esi + edi]
rcpss  xmm0, dword ptr [esi]
rcpss  xmm0, xmm1
rsqrtps  xmm0, xmm1
rsqrtps  xmm0, xmmword ptr [esi + edi]
rsqrtps  xmm0, xmmword ptr [esi]
rsqrtss  xmm0, dword ptr [esi + edi]
rsqrtss  xmm0, dword ptr [esi]
rsqrtss  xmm0, xmm1
sfence
shufpd  xmm0, xmm1, 0xa
shufpd  xmm0, xmmword ptr [esi + edi], 0xa
shufpd  xmm0, xmmword ptr [esi], 0xa
shufps  xmm0, xmm1, 0xa
shufps  xmm0, xmmword ptr [esi + edi], 0xa
shufps  xmm0, xmmword ptr [esi], 0xa
sqrtpd  xmm0, xmm1
sqrtpd  xmm0, xmmword ptr [esi + edi]
sqrtpd  xmm0, xmmword ptr [esi]
sqrtps  xmm0, xmm1
sqrtps  xmm0, xmmword ptr [esi + edi]
sqrtps  xmm0, xmmword ptr [esi]
sqrtsd  xmm0, qword ptr [esi + edi]
sqrtsd  xmm0, qword ptr [esi]
sqrtsd  xmm0, xmm1
sqrtss  xmm0, dword ptr [esi + edi]
sqrtss  xmm0, dword ptr [esi]
sqrtss  xmm0, xmm1
stmxcsr  dword ptr [esi + edi]
stmxcsr  dword ptr [esi]
subpd  xmm0, xmm1
subpd  xmm0, xmmword ptr [esi + edi]
subpd  xmm0, xmmword ptr [esi]
subps  xmm0, xmm1
subps  xmm0, xmmword ptr [esi + edi]
subps  xmm0, xmmword ptr [esi]
subsd  xmm0, qword ptr [esi + edi]
subsd  xmm0, qword ptr [esi]
subsd  xmm0, xmm1
subss  xmm0, dword ptr [esi + edi]
subss  xmm0, dword ptr [esi]
subss  xmm0, xmm1
ucomisd  xmm0, qword ptr [esi + edi]
ucomisd  xmm0, qword ptr [esi]
ucomisd  xmm0, xmm1
ucomiss  xmm0, dword ptr [esi + edi]
ucomiss  xmm0, dword ptr [esi]
ucomiss  xmm0, xmm1
unpckhpd  xmm0, xmm1
unpckhpd  xmm0, xmmword ptr [esi + edi]
unpckhpd  xmm0, xmmword ptr [esi]
unpckhps  xmm0, xmm1
unpckhps  xmm0, xmmword ptr [esi + edi]
unpckhps  xmm0, xmmword ptr [esi]
unpcklpd  xmm0, xmm1
unpcklpd  xmm0, xmmword ptr [esi + edi]
unpcklpd  xmm0, xmmword ptr [esi]
unpcklps  xmm0, xmm1
unpcklps  xmm0, xmmword ptr [esi + edi]
unpcklps  xmm0, xmmword ptr [esi]
xorpd  xmm0, xmm1
xorpd  xmm0, xmmword ptr [esi + edi]
xorpd  xmm0, xmmword ptr [esi]
xorps  xmm0, xmm1
xorps  xmm0, xmmword ptr [esi + edi]
xorps  xmm0, xmmword ptr [esi]
```

