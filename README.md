# The Net Ninja - Animação com css

## Link Playlist

[CSS Animation Tutorial](https://www.youtube.com/watch?v=jgw82b5Y2MU)


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