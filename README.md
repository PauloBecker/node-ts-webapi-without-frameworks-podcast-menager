# 🎙️ Podcast Manager

![Node Version](https://shields.io)
![TypeScript](https://shields.io)
![Status](https://shields.io)

O Podcast Manager é uma API REST robusta construída em Node.js, projetada para centralizar e organizar episódios de podcasts em vídeo. O projeto segue uma interface visual inspirada no estilo "Netflix", onde os conteúdos são categorizados e facilmente acessíveis.
🚀 Funcionalidades

    Listagem Completa: Retorna todos os episódios disponíveis no banco de dados.
    Filtragem Inteligente: Permite buscar episódios específicos através do nome do podcast via query strings.
    Categorização: Suporte a múltiplas categorias como saúde, fitness, mentalidade, humor, entre outras.

🛠️ Tecnologias Utilizadas

```
- **[Node.js](https://nodejs.org):** Ambiente de execução principal.
*   [TypeScript](https://typescriptlang.org) (^6.0.2) - Tipagem forte para maior segurança.
*   [TSUP](https://egoist.dev) (^8.5.1) - Ferramenta de build extremamente veloz.
*   [TSX](https://tsx.is) (^4.21.0) - Executor TypeScript direto para desenvolvimento.
*   [@types/node](https://npmjs.com) (^25.6.0) - Definições de tipo para APIs nati
```
📂 Estrutura de Pastas
O projeto utiliza uma arquitetura baseada em camadas para facilitar a manutenção:
```
src/
├── controllers/    # Gerenciamento de rotas e respostas HTTP
├── models/         # Interfaces e contratos de dados (TS)
├── repositories/   # Persistência de dados (JSON)
├── services/       # Regras de negócio e lógica de filtragem
├── utils/          # Constantes como Status Codes e Content Types
└── server.ts       # Ponto de entrada da aplicação

```

📝 Como Consumir a API
```
1. Crie um arquivo `.env` na raiz do projeto.

2. Listar todos os episódios
Retorna a lista completa de episódios formatada com metadados.

    URL: http://localhost:3636/api/list
    Método: GET

3. Filtrar episódios por nome
Filtra os episódios com base no nome do podcast passado pela URL.

    URL: http://localhost:3333/api/episode?p=flow
    Método: GET
```
📊 Formato do Dado (JSON)
Cada episódio segue o contrato abaixo:
json
```
{
  "podcastName": "Flow",
  "episode": "CBUM - Flow #319",
  "videoID": "pQSuQmUfS30",
  "cover": "https://i.ytimg.com/vi/pQSuQmUfS30/hq720.jpg",
  "link": "https://www.youtube.com/watch?v=pQSuQmUfS30",
  "category": ["saúde", "bodybuilder"]
}
```
⚙️ Como Executar o Projeto - Configuração Local

1 - Clone o repositório:
```
    bash
    git clone https://github.com/PauloBecker/node-ts-webapi-without-frameworks-podcast-menager/
```
2 - Instalar as dependências:
```
    bash

    npm install
```
  3 - Executar em modo de desenvolvimento:
  ```
    bash

    npm run start:dev
```
   🛠️ Scripts Disponíveis
```
O projeto utiliza o `tsx` para execução rápida e `tsup` para build de produção.

- `npm run start:dev`: Executa o servidor em modo de desenvolvimento.
- `npm run start:watch`: Executa o servidor em modo "watch" (reinicia automaticamente a cada alteração no código).
- `npm run dist`: Compila o projeto de TypeScript para JavaScript otimizado na pasta `dist`.
- `npm run start:dist`: Faz o build completo e executa a versão final de produção.
```

🏗️ Exemplo de Implementação de Rota
O núcleo da aplicação utiliza o módulo nativo http para roteamento dinâmico:
typescript
```
const baseUrl = request.url?.split("?")[0];

if(request.method === HttpMethods.GET && baseUrl === Routes.LIST) {
    await getListEpisodes(request, response);
}

Use o código com cuidado.
```
✨ Desenvolvido por [Paulo Becker - DIO]
