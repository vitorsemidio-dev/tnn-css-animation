# The Net Ninja - Animação com css

## Link Playlist

[CSS Animation Tutorial](https://www.youtube.com/watch?v=jgw82b5Y2MU&list=PL4cUxeGkcC9iGYgmEd2dm3zAKzyCGDtM5)


### Sintaxe
```
 animation: name duration timing-function delay iteration-count direction fill-mode;
```

## Translate

Movimenta o elemento em um determinado sentido. Opções são **translateX**, **translateY** nos respectivos eixos. Valores positivos passados por parâmetros movimenta o elemento para direita e baixo, respectivamente. Também é possível utilizar somente **translate** passando 1 ou 2 argumentos.

```css
.translate-1 {
    transform: translateX(100px);
}

.translate-2 {
    transform: translateY(100px);
}

.translate-3 {
    transform: translate(40px, 100px);
}
```

## Scale

Responsável por aumentar ou diminuir a escala do elemento. Podendo fazê-lo crescer/encolher no eixo X ou Y com **scaleX** e **scaleY**, respectivamente. Valores acima de 1 fazem-no crescer, para reduzi-lo é necessário passar um valor menor que 1. Se utilizar a função **scale** é possível passar 1 ou dois argumentos. Se passar somente 1, ele irá aplicar em ambos os eixos, se preencher os dois, será aplicado o primeiror valor para o eixo X e o segundo para o eixo Y.

```css
.scale-1 {
    transform: scale(0.5);
}

.scale-2 {
    transform: scale(2.5, 0.7);
}

.scale-3 {
    transform: scaleX(1.7);
}
```

## Rotate

Rotaciona o elemento em um determinado eixo.

```css
.rotate-1 {
    transform: rotateX(80deg);
}

.rotate-2 {
    transform: rotateY(80deg);
}

.rotate-3 {
    transform: rotateZ(80deg);
}
```

## Transform em série

Também é possível aplicar o transform utilizando mais de uma função em sequência.

```css
.all-1 {
    transform: translateX(100px) scale(0.5) rotateX(80deg);
}

.all-2 {
    transform: translateY(100px) scale(2.5, 0.7) rotateY(40deg);
}

.all-3 {
    transform: translate(40px, 100px) scaleX(1.7) rotateZ(80deg);
}
```

## Transitions

```css
.example {
    transition: [transition-property] [transition-duration] [transition-timing-function] [transition-delay];
}
```

```css

.circle-1 {
    transition: background-color 1s, transform 2s 1s;
}

.circle-2 {
    transition: background-color 2s 1s, transform 0.5;
}

.circle-3 {
    transition: 2s;
}

.circle-4 {
    background-color: teal;
    transition: transform 1s 1s linear;
}

.circle-5 {
    background-color: teal;
    transition: transform 1s 1s ease-in;
}
```

## Keyframes

```css
.mario {
  position: absolute;
  top: -40px;
  left: 0;

  animation-name: drive;
  animation-duration: 3s;
}

@keyframes drive {
  from {
    transform: translate(0)
  }
  to {
    transform: translate(500px);
  }
}

```

## Animation Fill Mode

```css
@keyframes drive {
  from {
    transform: translate(200px)
  }
  to {
    transform: translate(500px);
  }
}
```

### Sintaxe
```
animation-fill-mode: none | forwards | backwards | both | initial | 
inherit;
```

### Exampla forwards

```css
animation-fill-mode: forwards;
```

<img src=".github/mario-forwards.png" alt="imagem">

### Exampla backwards

```css
animation-fill-mode: backwards;
```

<img src=".github/mario-backwards.png" alt="imagem">


## Direção

```
animation-direction: alternate alternate-reverse normal reverse initial inherit unset;
```

## Timing Function

[Cubic Bezier](https://cubic-bezier.com/#.17,.67,.83,.67)


[W3schools](https://www.w3schools.com/cssref/css3_pr_animation-timing-function.asp)
Função   | Descrição
--------- | ------
linear | The animation has the same speed from start to end
ease | Default value. The animation has a slow start, then fast, before it ends slowly
ease-in | The animation has a slow start
ease-out | The animation has a slow end
ease-in-out | The animation has both a slow start and a slow end

```css
.timing1 {animation-timing-function: linear;}
.timing2 {animation-timing-function: ease;}
.timing3 {animation-timing-function: ease-in;}
.timing4 {animation-timing-function: ease-out;}
.timing5 {animation-timing-function: ease-in-out;}

.cubic1 {animation-timing-function: cubic-bezier(0,0,1,1);}
.cubic2 {animation-timing-function: cubic-bezier(0.25,0.1,0.25,1);}
.cubic3 {animation-timing-function: cubic-bezier(0.42,0,1,1);}
.cubic4 {animation-timing-function: cubic-bezier(0,0,0.58,1);}
.cubic5 {animation-timing-function: cubic-bezier(0.42,0,0.58,1);}
```
