# <span style="color: #00FF00">Trasformação 2D</span> 
- É possível mover, girar, dimensionar e inclinar elementos
## Métodos:
### <span style="color: #1E90FF">Translate()</span> 
- Na horizontal, permite deslocar um box na horizontal:
	```css
	seletor { trasnform: trasnlateX(x)};
	```
- Na vertical:
```css
seletor { trasnform: trasnlateY(y)};
```
- Na vertical e na horizontal:
```css
seletor { trasnform: trasnlate(x,y)};
```
---
## <span style="color: #00FF00"> rotate()</span> 
-  Rotacionar o ângulo:
	```css
	seletor { trasnform: rotate(a)};
```
## <span style="color:violet">scale()</span>  
- No x (horizontal):
	```css
	seletor { trasnform: scalex(n)};
```
- Na vertical
```css
	seletor { trasnform: scaleY(n)};
```
- Na vertical e na horizontal:
```css
	seletor { trasnform: scale(n,m)};
```

## <span style="color:red">skew()</span> 
- No horizontal:
```css
	seletor { trasnform: skewX(a)};
```
- vertical:
```css
	seletor { trasnform: skewY(a)};
```
- Vertical e horizontal:
```css
	seletor { trasnform: skew(a,b)};
```

## <span style="color:yellow">matrix()</span>
- Todas as trasnformações possíveis:
```css
	matrix(scaleX(),SkewY(), sclaeY(), trasnlateX(),translateY())
```

---
# TRANSIÇÕES CSS
- Permite criar transições ao definir uma mudança de valor de uma propriedade CSS, de modo que ela ( a mudança de valor) ocorra de forma suave, em um espaço de tempo especificado.
## Propriedade de tranasição:
- Transition
- transition-delay
- Transition-duration
- Transition-property
- Transution-timing-function