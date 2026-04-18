
# Podcast Menager

### Descrição
Um app ao estilo netflix, aonde possa centralizar diferentes episódios podcasts separados por categoria

### Domínio
Podcasts feitos em vídeo

### Features
    - Listar os episódios podcasts em sessões se categorias
        -[saúde, fitness, mentalidade, humor]
    -Filtrar episódios por nome de podcast

## Como

#### Feature:
    Listar os episódios podcasts em sessões se categorias

### Como vou implementar:

Vou retornar em uma api rest (json) o nome podcast, nome do episódio, imagem de capa, link, category

```js
[
    {
        podcastName: "flow",
        episode: "CBUM - Flow #319",
        videoID: "pQSuQmUfS30",
        cover: "https://i.ytimg.com/vi/pQSuQmUfS30/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDrkn0FBDuol1SvDUAOsK-qXsGhfQ",
        link: "https://www.youtube.com/watch?v=pQSuQmUfS30/maxresdefault.jpg",
        category: ["saúde","bodybuilder"]
    },
    {
        podcastName: "flow",
        episode: "RUBENS BARRICHELLO - Flow #339",
        videoID: "4KDGTdiOV4I",
        cover: "https://i.ytimg.com/vi/4KDGTdiOV4I/maxresdefault.jpg",
        link: "https://www.youtube.com/watch?v=4KDGTdiOV4I&pp=ygUfZmxvdyBwb2RjYXN0IHJ1YmVucyBiYXJyaWNoZWxsbw%3D%3D",
        category: ["esporte","corrida"]
    },

]
```