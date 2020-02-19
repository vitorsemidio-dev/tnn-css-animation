# The Net Ninja - Animação com css

## Link Playlist

[CSS Animation Tutorial](https://www.youtube.com/watch?v=jgw82b5Y2MU)


## Translate

Movimenta o elemento em um determinado sentido. Opções são **translateX**, **translateY** nos respectivos eixos. Valores positivos passados por parâmetros movimenta o elemento para direita e baixo, respectivamente. Também é possível utilizar somente **translate** passando 1 ou 2 argumentos.

```css
.baixo-direita-100 {
    transform: translateX(100px);
    transform: translateY(100px);
}

.baixo-esquerda-100 {
    transform: translate(-100px, 100px);
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