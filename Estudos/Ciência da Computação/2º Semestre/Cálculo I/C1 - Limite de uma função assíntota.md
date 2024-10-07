Como vimos na última aula, <span style="color:#7317cf">assíntota</span> é uma reta que se aproxima de uma curva/função, confirme x se aproxima de um determinado valor, em que ficamos restringidos as assíntotas verticais.

Ex da última aula:

b) $lim_{x\to0} \left(\frac{{x}}{x^2}\right)= {+∞}$



```functionplot
---
title: Assíntota
xLabel: x
yLabel: y
bounds: [-11,10,-8,5]
disableZoom: false
grid: true
---
f(x) = x/x^2

```

c) $lim_{x\to-1} \left(\frac{{5x}+{2}}{x+1}\right)= {-∞}$


```functionplot
---
title: 
xLabel: x
yLabel: y
bounds: [-11,10,-8,5]
disableZoom: false
grid: true
---
f(x) = (5x+2)/(x+1)
```

Se você notar as funções e analisar virtualmente a localização das retas, perceberá que f(x) pode assumir valores arbitrariamente grandes em termos absolutos ou não, a medida que se aproxima da assíntota. Uma maneira de identificar as assíntotas verticais é por meio das indeterminações do tipo 1/0, em que a função assume valores grandes ao se aproximar, de ambos os lados, do valor(es) que resulta(m) na(o) indeterminação(ões).

<span style="color:#7317cf">Testar se a reta x = 2 é uma assíntota vertical da função:</span>

  ${f(x)} = \left(\frac{1}{x^2+8x-20}\right)$
  

```functionplot
---
title: 
xLabel: 2
yLabel: x
bounds: [-11,10,-8,5]
disableZoom: false
grid: true
---
f(x) = (1)/(x^2+8x-20)
```

$lim_{x\to2^+}\left(\frac{1}{(2^+)^2 + 8(2^+)-20}\right)= \frac{1}{(4^+) + (16^+) - 20} = \frac{1}{0^+} = {+∞})$


$lim_{x\to2^-} \left(\frac{1}{(2^-)^2 + 8(2^-)-20}\right)= \frac{1}{(4^-) + (16^-) - 20}\frac{1}{0^-} = {-∞})$








  



