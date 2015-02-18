---
title: Differential calculus
layout: post
date: 2015-01-31 22:00:00
postTitle: Integration techniques
categories: integral
---

-------

# Integration by parts

--------

## Deriving integration by parts formula

微分におけるproduct rule　を思い出しましょう
<div class="panel">
$$\frac{d}{dx}(f(x)g(x))=f'(x)g(x)+f(x)g'(x)$$
</div>

\\(f(x)g(x)\\)は右辺を積分したものになりますから
$$f(x)g(x)=\int f'(x)g(x)dx + \int f(x)g'(x)dx$$
両辺から\\(\int f'(x)g(x)dx\\)を引きます
$$f(x)g(x)-\int f'(x)g(x)dx = \int f(x)g'(x)dx$$
両辺を入れ替えます
<div class="panel">
$$\int f(x)g'(x)dx = f(x)g(x)-\int f'(x)g(x)dx$$
</div>

この規則を使って積分を行います

例1

$$\int x \cos x dx=?$$
$$f(x)=x \quad f'(x)=1 \quad g(x)= \sin x \quad g'(x)= \cos x$$
これから
$$\int x \cos x dx=x \cdot \sin x - \int (1 \cdot \sin x)dx$$
$$\quad = x \cdot \sin x - (-\cos x) 
= x \cdot \sin x + \cos x + C$$

例2

$$\int (\ln x) dx=?$$
これを書き換えます
$$\int (\ln x) dx=\int (\ln x \cdot 1) dx$$
$$f(x)=\ln x \quad f'(x)=\frac{1}{x} \quad g(x)= x \quad g'(x)=1$$
これから
$$\int (\ln x \cdot 1) dx 
=x \cdot \ln x - \int (\frac{1}{x} \cdot x)dx
=x \cdot \ln x - x + C$$

例3

$$\int (x^2e^x) dx=?$$
$$f(x)=x^2 \quad f'(x)=2x \quad g(x)= e^x \quad g'(x)=e^x$$
これから
$$\int (x^2e^x) dx=x^2e^x-\int (2xe^x) dx
=x^2e^x-2\int (xe^x) dx$$
\\(\int (xe^x) dx\\)について規則から
$$f(x)=x \quad f'(x)=1 \quad g(x)= e^x \quad g'(x)=e^x$$
したがって
$$\int (x^2e^x) dx=x^2e^x-\int (2xe^x) dx
=\int (x^2e^x) dx=x^2e^x-2\int (xe^x) dx
=x^2e^x - (2xe^x-2\int (1 \cdot e^x)dx) 
=x^2e^x - 2xe^x + 2e^x+C$$

例4

$$\\int (e^x \cos x) dx=?$$
$$f(x)=e^x \quad f'(x)=e^x \quad g(x)= \sin x \quad g'(x)=\cos x$$
よって
$$\int (e^x \cos x) dx=e^x \sin x - \int (e^x \sin x)dx$$
ここで
$$\int (e^x \sin x)dx=?$$
$$f(x)=e^x \quad f'(x)=e^x \quad g(x)= -\cos x \quad g'(x)=\sin x$$
$$\int (e^x \sin x)dx=-e^x\cos x +\int (e^x \cos x)$$
$$\int (e^x \cos x) dx=e^x \sin x - \int (e^x \sin x)dx
=e^x \sin x + e^x\cos x - \int (e^x \cos x)$$
$$2\int (e^x \cos x) dx=e^x \sin x + e^x\cos x$$
$$\int (e^x \cos x) dx=\frac{e^x \sin x + e^x\cos x}{2}+C$$

-------

# U-substitution

-------

不定積分
$$\int (3x^2+2x)e^{(x^3+x^2)} dx$$
これの解き方としてu-substitutionというテクニックを使います

注目するのは\\(3x^2+2x\\) は \\(x^3+x^2\\) の導関数という点です

$$u=x^3+x^2$$
$$\frac{du}{dx}=3x^2+2x \to du = (3x^2+2x)dx$$
とします

問題の不定積分を書き換えます
$$\int (3x^2+2x)e^{(x^3+x^2)} dx = \int (3x^2+2x)dx e^{(x^3+x^2)}
= \int du e^{u} = \int e^{u}du $$
$$\quad = e^{u} + C = e^{x^3+x^2} + C$$

例１

<div class="panel">
$$\int \frac{4x^3}{x^4 + 7}dx$$
</div>

$$u=x^4 + 7$$
$$\frac{du}{dx}=4x^3 \to du=4x^3dx$$
問題を書き換えます
$$\int \frac{4x^3}{x^4 + 7}dx=\int \frac{4x^3dx}{x^4 + 7}
=\int \frac{du}{u}=\frac{1}{u}du$$
$$\quad = ln|u| + C = ln|x^4 + 7| + C$$

例2
<div class="panel">
$$\int \sqrt{7x+9}dx$$
</div>
$$u=7x+9$$
$$\frac{du}{dx}=7 \to du=7dx$$

ここで７という数字を使うために少し工夫します
$$\int \frac{1}{7}\cdot 7\sqrt{7x+9}dx 
=\frac{1}{7} \int 7dx\sqrt{7x+9}$$
$$\quad = \frac{1}{7} \int \sqrt{u}du 
= \frac{1}{7} \int u^{\frac{1}{2}}du 
=\frac{1}{7}(\frac{2}{3}u^{\frac{3}{2}}+C)
=\frac{2}{21}u^{\frac{3}{2}} + C$$
$$\quad = \frac{2}{21}(7x+9)^{\frac{3}{2}} + C$$

例3
<div class="panel">
$$\int \frac{\pi}{x\ln x}dx$$
</div>
$$u=\ln x$$
$$\frac{du}{dx}=\frac{1}{x} \to du={1}{x}dx$$
問題を書き換えます
$$\int \frac{\pi}{x\ln x}dx
=\pi \int \frac{1}{\ln x}\frac{1}{x}dx
=\pi \int \frac{1}{u}du$$
$$ \quad
=\pi ln|u| + C
=\pi ln|\ln x| + C$$

例4
<div class="panel">
$$\int_{0}^{1}x^2 2^{x^{3}} dx$$
</div>
$$\frac{d}{dx}e^x=e^x$$
$$\int e^x dx = e^x + C$$
$$2=e^{\ln2} \to 2^{x^3}=(e^{\ln2})^{x^3}=e^{x^{3}\ln2}$$
問題を書き換えます
$$\int_{0}^{1}x^2 e^{x^{3}\ln2} dx$$
u-subsutitution
$$u=x^{3}\ln2$$
$$\frac{du}{dx}=3x^2 \ln2=x^2 3\ln2 =x^2 \ln2^3 = \ln8 x^2
\to du=\ln8 x^2dx$$
$$\intx^2 e^{x^{3}\ln2} dx
=\frac{1}{\ln8} \int \ln8 x^2 e^{x^{3}\ln2} dx
=\frac{1}{\ln8} \int e^{u}du
=\frac{1}{\ln8}e^{u}+C=\frac{1}{\ln8}e^{x^{3}\ln2}+C$$
$$\int_{0}^{1}x^2 2^{x^{3}} dx
=\frac{1}{\ln8}e^{1^{3}\ln2}-\frac{1}{\ln8}e^{0^{3}\ln2}
=\frac{1}{\ln8}*2 - \frac{1}{\ln8}*1
=\frac{1}{\ln8}$$

例5
<div class="panel">
$$\int \frac{2^{\ln x}}{x} dx = \int \frac{1}{x}2^{\ln x}dx$$
</div>
$$u=\ln x$$
$$du = \frac{1}{x}dx$$

$$\int \frac{1}{x}2^{\ln x}dx
=\int 2^{u}du
=\int (e^{\ln2})^{u}du
=\int (e^{(\ln2)u}du$$
$$\qquad \int e^{au}du=\frac{1}{a}e^{au}+C$$
$$=\frac{1}{\ln2}e^{u\ln2}+C$$
$$ \qquad a\ln b = \ln b^a \to u\ln2=\ln 2^{u}$$
$$=\frac{1}{\ln2}2^{u}+C$$
$$=\frac{1}{\ln2}2^{\ln x}+C$$

例6
<div class="panel">
$$\int (x+3)(x-1)^5 dx $$
</div>
$$u=x-1 \to x= u+1$$
$$du = dx$$

$$\int (x+3)(x-1)^5 dx
=\int (u+1+3)u^5 du
=\int (u+4)u^5 du
=\int (u^6+4u^5) du
=\frac{u^7}{7}+\frac{4u^6}{6} + C$$
$$=\frac{(x-1)^7}{7}+\frac{2}{3}(x-1)^6 + C$$

例7
<div class="panel">
$$\int_{0}^{\sqrt{\pi}}x\sin(x^2)dx$$
</div>
$$u=x^2$$
$$du = 2xdx$$
置き換えます
$$\frac{1}{2}\int_{0}^{\sqrt{\pi}}2x\sin(x^2)dx
=\frac{1}{2}\int_{u=0}^{u=\pi}\sin(u)du
=\frac{1}{2}[-\cos u ]_{0}^{\pi}$$
$$=\frac{1}{2}[-\cos \pi + \cos 0]
=\frac{1}{2}[1 + 1]=1$$

例8
<div class="panel">
$$\int \frac{\cos(5x)}{e^{\sin(5x)}}dx$$
</div>
$$u=\sin(5x)$$
$$\frac{d}{dx}=5\cos(5x) \to du=5\cos(5x)dx$$

置き換えると
$$\int \frac{\cos(5x)}{e^{\sin(5x)}}dx
=\frac{1}{5}\int \frac{5\cos(5x)}{e^{\sin(5x)}}dx
=\frac{1}{5}\int \frac{1}{e^u}du
=\frac{1}{5}\int e^{-u}du
$$
ここで-uを
$$w=-u$$
$$dw=-du$$

置き換えます
$$
=(-1)\frac{1}{5}\int e^{-u}du(-1)
=-\frac{1}{5}\int e^{w}dw
=-\frac{1}{5}e^{w}+C
=-\frac{1}{5}e^{-u}+C
=-\frac{1}{5}e^{-\sin(5x)}+C
$$

---------

# Reverse chain rule

<div class="panel">
  <h3>Chain Rule</h3>
  $$\frac{d}{dx}g(f(x))=g'(f(x)) \cdot f'(x)$$
</div>
$$\qquad \downarrow$$
<div class="panel">
  <h3>Reverse Chain Rule</h3>
  $$\int g'(f(x)) \cdot f'(x) dx = g(f(x)) + C$$
</div>

例１

<div class="panel">
  $$\int (\sin x)^2 \cos x dx = ?$$
</div>

$$u=\sin x$$
$$\frac{du}{dx}=\cos x \to du=\cos x dx$$

$$\int (\sin x)^2 \cos x dx 
=\int (u)^2 du = \frac{u^3}{3} + C
=\frac{(\sin x)^3}{3} + C$$

例2

<div class="panel">
  $$\int \frac{x}{2}\sin(2x^2+2) dx = ?$$
</div>

$$f(x)=2x^2 + 2$$
$$f'(x)=4x$$

$$\int \frac{x}{2}\sin(2x^2+2) dx
=\frac{1}{2}\frac{1}{4} \int 4x \sin(2x^2+2) dx
=\frac{1}{8}\int f'(x) \sin(f(x)) dx
=\frac{1}{8}(-cos(f(x)))+C
=\frac{1}{8}(-cos(2x^2 + 2))+C$$

例3

<div class="panel">
  $$\int \tan x dx = ?$$
</div>

$$\int \tan x dx 
=\int \frac{\sin x}{\cos x}dx
=\int \sin x \frac{1}{\cos x}dx$$

$$\qquad \int \frac{1}{x}= \ln|x| + c$$
$$\qquad \int f'(x)\frac{1}{f(x)}=\ln|f(x)|+C$$
$$\qquad f(x)= \cos x$$
$$\qquad f'(x)= -\sin x $$ 

$$
=-\ln|\cos x| + C
$$

---------

# Integration using trigonometric identities

例1
<div class="panel">
  $$\int \cos^3 x dx = ?$$
</div>

$$
\int \cos^3 x dx = \int (\cos x)(\cos^2 x)dx
= \int (\cos x)(1 - \sin^2 x)dx
$$

$$\qquad u=\sin x$$
$$\qquad du = \cos x dx$$

$$
=\int (1-u^2)du
= u - \frac{1}{3}u^3 + C
= \sin x - \frac{1}{3}sin^3 x + C
$$

例2
<div class="panel">
  $$\int \sin^2 x \cos^3 x dx = ?$$
</div>

$$
\int \sin^2 x \cos^3 x dx = 
\int \sin^2 x \cos^2 x \cos x dx
=\int \sin^2 x (1-\sin^2 x) \cos x dx
=\int (sin^2 x - \sin^4 x) \cos x dx 
$$

$$\qquad u=\sin x$$
$$\qquad du = \cos x dx$$

$$
=\int (u^2 - u^4) du
=\frac{u^3}{3}-\frac{u^5}{5} + C
=\frac{sin^3 x}{3}-\frac{sin^5 x}{5} + C
$$

例3
<div class="panel">
  $$\int \sin^4 x dx = ?$$
</div>

$$\qquad sin^2 x = \frac{1}{2}(1 - \cos 2x)$$

$$
\int \sin^4 x dx = \int (\sin^2 x )^2 dx
=\int (\frac{1}{2}(1 - \cos 2x))^2 dx
=\frac{1}{4} \int (1 - 2\cos 2x + \cos^2 2x) dx
$$

$$ \qquad \cos^2 2x = \frac{1}{2}(1 + cos 4x)$$
$$
=\frac{1}{4} \int (1-2\cos 2x + \frac{1}{2} + \frac{1}{2}\cos 4x)dx
=\frac{1}{4} \int (\frac{3}{2}-2\cos 2x+\frac{1}{8}4\cos 4x) dx
=\frac{1}{4} (\frac{3}{2}x - \sin 2x + \frac{1}{8} \sin 4x) + C
$$

-----------

# Trigonometric substitution

例1
<div class="panel">
  $$\int \frac{1}{\sqrt{1-x^2}} dx = ?$$
</div>

$$\qquad -1 \lt x \lt 1 $$
$$\qquad x = \sin \theta$$
$$\qquad dx = \cos \theta d\theta$$
$$\qquad \theta = \arcsin x$$

$$
\int \frac{1}{\sqrt{1-x^2}} dx
=\int \frac{\cos \theta}{\sqrt{(1-sin^2 \theta)}}d\theta
=\int \frac{\cos \theta}{\sqrt{cos^2 \theta}}d\theta
=\int \frac{\cos \theta}{|cos \theta|}d\theta
$$

$$\qquad \cos \theta \ge 0 $$
$$
=\int d\theta
=\theta + C
=\arcsin x + C
$$

例２
<div class="panel">
  $$\int \frac{\pi}{\sqrt{8-2x^2}} dx = ?$$
</div>

$$\qquad a^2 - x^2 \to x=a\sin \theta$$
$$\qquad a^2 - a^2\sin^2 \theta) = a(1-sin^2 \theta)$$
$$\qquad x = 2\sin \theta$$
$$\qquad dx = 2\cos \theta d\theta$$
$$\qquad \theta = \arcsin(\frac{x}{2})$$
$$\qquad 8 - 2x^2 = 2(4-x^2)= 2(2^2-2^2sin^2 \theta) 
= 2\cdot 2^2(1-\sin^2 \theta)=8\cos^2 \theta$$

$$\int \frac{\pi}{\sqrt{8-2x^2}} dx 
=\pi \int \frac{2\cos \theta}{\sqrt{8\cos^2 \theta}} d\theta
=\pi \int \frac{2\cos \theta}{2\sqrt{2}\cos\theta} d\theta
=\frac{\pi}{\sqrt{2}}\int d\theta
=\frac{\pi}{\sqrt{2}}\theta + C
=\frac{\pi}{\sqrt{2}}\arcsin(\frac{x}{2}) + C$$

例3
<div class="panel">
  $$\int \frac{1}{\sqrt{3-2x^2}} dx = ?$$
</div>

変形します
$$\int \frac{1}{\sqrt{3-2x^2}} dx 
=\int \frac{1}{\sqrt{3(1-\frac{2}{3}x^2)}} 
$$

$$\qquad \frac{2}{3}x^2=sin^2 \theta$$
$$\qquad \frac{\sqrt{2}}{\sqrt{3}}x^2=sin \theta$$
$$\qquad \theta = \arcsin(\frac{\sqrt{2}}{\sqrt{3}}x)$$
$$\qquad x=\frac{\sqrt{3}}{\sqrt{2}}\sin \theta$$
$$\qquad dx=\frac{\sqrt{3}}{\sqrt{2}}\cos \theta d\theta$$

$$
=\int \frac{\frac{\sqrt{3}}{\sqrt{2}}\cos \theta d\theta}
{\sqrt{3(1-sin^2 x)}}
=\int \frac{\frac{\sqrt{3}}{\sqrt{2}}\cos \theta d\theta}
{\sqrt{3(cos^2 x)}}
=\int \frac{\frac{\sqrt{3}}{\sqrt{2}}\cos \theta d\theta}
{\sqrt{3}cos x)}
=\int \frac{1}{\sqrt{2}}d\theta
=\frac{1}{\sqrt{2}} \int d \theta
$$
$$
=\frac{1}{\sqrt{2}}\theta + C
=\frac{1}{\sqrt{2}}\arcsin(\frac{\sqrt{2}}{\sqrt{3}}x) + C
$$

例4
<div class="panel">
  $$\int x^3 \sqrt{9-x^2} dx = ?$$
</div>

$$\qquad 9-x^2 = 3^2 - x^2$$
$$\qquad x=a\sin \theta = 3\sin \theta \to \sin \theta = \frac{x}{3}$$
$$\qquad dx = 3\cos \theta d\theta$$
$$\qquad 3^2 - 3^2 \sin^2 \theta = 9(1-sin^2 \theta)$$
$$\qquad \sqrt{9-x^2}=\sqrt{9\cos^2 \theta}=3\cos \theta$$

$$
\int x^3 \sqrt{9-x^2} dx
=\int 27\sin^3 \theta 3\cos \theta \cdot 3\cos \theta d\theta
$$
$$
=243 \int sin^3 \theta \cos^2 \theta d\theta
$$
$$
=243 \int sin^2 \theta \cos^2 \theta \sin \theta d\theta
$$
$$
=243 \int (1-cos^2 \theta) \cos^2 \theta \sin \theta d\theta
$$

$$\qquad u= \cos \theta$$
$$\qquad du = -\sin \theta d\theta$$

$$
=-243 \int (1-cos^2 \theta) \cos^2 \theta -\sin \theta d\theta
$$
$$
=-243 \int (1-u^2) \u^2  du
=-243 \int(u^2 - u^4) du
=-243(\frac{u^3}{3}-\frac{u^5}{5}) + C
$$

$$\qquad \sin \theta = \frac{x}{3}$$ 
$$\qquad \cos \theta = \frac{\sqrt{9-x^2}}{3} 
=\sqrt{\frac{1}{9}(9-x^2)}
= (1-\frac{x^2}{9})^{\frac{1}{2}}=u$$
$$
=243(\frac{u^5}{5}-\frac{u^3}{3}) + C
$$
$$
=243(\frac{(1-\frac{x^2}{9})^{\frac{5}{2}}}{5}
-\frac{(1-\frac{x^2}{9})^{\frac{3}{2}}}{3}) + C
$$

例5 
<div class="panel">
  $$\int \frac{1}{9 + x^2} dx = ?$$
</div>

$$\qquad a^2 - x^2 \to x = a\sin \theta としてきましたが$$
$$\qquad a^2 + x^2 \to x = a\tan \theta とします$$
$$\qquad = a^2 + a^2\tan^2 \theta
=a^2(1 + tan^2 \theta)
=a^2(\frac{\cos^2 \theta}{\cos^2 \theta} 
   + \frac{\sin^2 \theta}{\cos^2 \theta})
=a^2(\frac{\cos^2 \theta + \sin^2 \theta}{\cos^2 \theta}) 
=a^2(\frac{1}{\cos^2 \theta}) 
=a^2\sec^2 \theta$$
$$\qquad 9+x^2 = 3^2 + x^2=3^2\sec^2 \theta$$
$$\qquad a = 3$$
$$\qquad x = 3\tan \theta$$
$$\qquad dx = 3\sec^2 \theta d\theta$$
$$\qquad \frac{x}{3}=\tan \theta$$
$$\qquad \theta = \arctan(\frac{x}{3})$$

$$\int \frac{1}{9 + x^2} dx 
=\int \frac{3\sec^2 \theta d\theta}{9\sec^2 \theta}
=\frac{1}{3}\int d\theta
=\frac{1}{3} \theta + C
$$
$$
=\frac{1}{3} \arctan(\frac{x}{3}) + C
$$ 

例6 
<div class="panel">
  $$\int \frac{1}{36 + x^2} dx = ?$$
</div>

まず変形します
$$=\int \frac{1}{36(1+\frac{x^2}{36})}$$

$$\qquad \frac{x^2}{36}= \tan^2 \theta 
\to \frac{x}{6} \to x=6\tan \theta$$
$$\qquad 1 + \tan^2 \theta = 1 + \frac{\sin^2 \theta}{\cos^2 \theta}
=\frac{\cos^2 \theta}{\cos^2 \theta} + \frac{\sin^2 \theta}{\cos^2 \theta}
=\frac{\cos^2 \theta + \sin^2 \theta}{\cos^2 \theta}
=\frac{1}{\cos^2 \theta}=sec^2 \theta$$
$$\qquad dx=6\sec^2 \theta d\theta$$
$$\qquad \arctan \frac{x}{6} = \theta$$

$$=\int \frac{6\sec^2 \theta d\theta}{36(1+\tan^2 \theta)}
=\int \frac{6\sec^2 \theta d\theta}{36\sec^2 \theta}
$$
$$
=\frac{1}{6}\int d\theta
$$
$$
=\frac{1}{6}\theta + C
=\frac{1}{6}\arctan(\frac{x}{6}) + C
$$ 

例7 
<div class="panel">
  $$\int \sqrt{6x-x^2 -5} dx = ?$$
</div>

これを変形します
$$
=\int \sqrt{-5 +9 -(x^2-6x +9)} dx
=\int \sqrt{4 - (x-3)^2} dx
=\int \sqrt{4(1 - \frac{(x-3)^2}{4}} dx
=\int 2 \sqrt{1-(\frac{x-3}{2})^2} dx 
$$

$$\qquad \cos^2 \theta = 1 - \sin^2 \theta$$
$$\qquad sin^2 \theta = (\frac{x-3}{2})^2 
\to \sin \theta = \frac{x-3}{2}$$
$$\qquad \theta = \arcsin(\frac{x-3}{2})$$ 
$$\qquad x = 2\sin \theta + 3$$
$$\qquad dx = 2\cos \theta d\theta$$

$$
=\int2 \sqrt{1-\sin^2 \theta} 2\cos \theta d\theta
=\int 4\cos^2 \theta d\theta
$$

$$\qquad \cos^2 \theta = \frac{1}{2}(1 - \cos2\theta)$$

$$
=\int 4 \cdot \frac{1}{2}(1 - \cos2\theta)d\theta
=\int 2(1 - \cos2\theta)d \theta
=\int(2-2\cos2\theta) d \theta
$$
$$
=2\theta-\sin 2\theta + C
$$  

$$\qquad \sin 2\theta = \sin(\theta + \theta)
= \sin \theta \cos \theta + \sin \theta + \cos \theta =
=2\sin \theta \cos \theta
$$

$$
=2\theta + 2\sin \theta \cos \theta + C
=2\theta + 2\sin \theta \sqrt{1-sin^2 \theta} + C
$$
$$=2\theta + 2\sin \theta \sqrt{1-sin^2 \theta} +C$$
$$=2\arcsin(\frac{x-3}{2}) + 2\frac{x-3}{2} \sqrt{1-(\frac{x-3}{2})^2}+C$$
$$=2\arcsin(\frac{x-3}{2})+\frac{x-3}{2}\sqrt{4} \sqrt{1-\frac{(x-3)^2}{4}}+C$$
$$=2\arcsin(\frac{x-3}{2})+\frac{x-3}{2}\sqrt{4-(x-3)^2}+C$$
$$=2\arcsin(\frac{x-3}{2})+\frac{x-3}{2}\sqrt{4-(x^2-6x+9)}+C$$
$$=2\arcsin(\frac{x-3}{2})+\frac{x-3}{2}\sqrt{6x-x^2-5)}+C$$

------------


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

</script>
