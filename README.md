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