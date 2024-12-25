<a id="readme-top"></a>

<div align="right">
	<spam>Idiomas</spam>
	
  [![Ícone da bandeira do Brasil. Clique para acessar o conteúdo em Português.](https://flagsapi.com/BR/flat/32.png)](README.md)
  [![Ícone da bandeira da America. Clique para acessar o conteúdo em Inglês.](https://flagsapi.com/US/flat/32.png)](README-EN.md)
  
</div>

# 🌐 Apresentação de slides do projeto

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=088df8&height=120&section=header"/>
<div align="center">

![Esta imagem contém um ícone de "play" azul no centro, indicando o início de uma apresentação de slides do projeto. O fundo possui formas geométricas em tons de azul escuro, com o texto "Apresentação de slides do projeto" no topo. Serve para guiar o usuário a clicar e iniciar a apresentação.](./assets/imagens/readme/logo-projeto.gif)

  <details>
  <summary>Descrição da Imagem</summary>
  Esta imagem contém um ícone de "play" azul no centro, indicando o início de uma apresentação de slides do projeto. O fundo possui formas geométricas em tons de azul escuro, com o texto "Apresentação de slides do projeto" no topo. Serve para guiar o usuário a clicar e iniciar a apresentação.
</details>

</div>
<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=088df8&height=120&section=footer"/>
			
---

<details>
<summary>Clique aqui para visualizar o índice</summary>
<br/>

:small_blue_diamond: [🌐 Apresentação de slides do projeto](#-apresenta%C3%A7%C3%A3o-de-slides-do-projeto)

:small_blue_diamond: [💡 Sobre o projeto](#-sobre-o-projeto)

:small_blue_diamond: [🌐Sobre o site escolhido](#-sobre-o-site-escolhido)

:small_blue_diamond: [📊Status do projeto](#-status-do-projeto)

:small_blue_diamond: [🚀 Resultado](#-resultado)

:small_blue_diamond: [🧱 Estrutura de arquivos/pastas](#-estrutura-de-arquivospastas)

:small_blue_diamond: [📐 Desenho do sistema](#-desenho-do-sistema)

:small_blue_diamond: [🏗️ Estrutura da Arquitetura e fluxo de interação](#%EF%B8%8F-estrutura-da-arquitetura-e-fluxo-de-intera%C3%A7%C3%A3o)

:small_blue_diamond: [⚔️ Tecnologias](#%EF%B8%8F-tecnologias)

:small_blue_diamond: [📜 Glossário](#-glossário)

:small_blue_diamond: [📋 Referências](#-refer%C3%AAncias)

:small_blue_diamond: [📝 Autores](#--autores)

:small_blue_diamond: [⚖️ Licença](#%EF%B8%8F-licen%C3%A7a)

</details>

# 💡 Sobre o projeto

⚡ O projeto AdrenalineStream API é uma API em JavaScript/NodeJS implementada em Docker na AWS para extrair informações relevantes de um site com conteúdo em formato RSS. Esta aplicação salva os dados em arquivo JSON dentro de um bucket S3, e permite a consulta do conteúdo salvo através de uma página HTML hospedada na cloud AWS.

---

<div align="center">
<img width=50% src="./assets/imagens/readme/logo_adrenaline.svg"/>
</div>

# 🌐 Sobre o site escolhido

- Com mais de 20 anos de experiência, o Adrenaline é hoje o maior site sobre hardware do Brasil. Diariamente, trazemos notícias, artigos e análises sobre componentes como placa de vídeo, placa-mãe, processadores e notebooks. Além disso, somos especializados no mercado de games, cobrindo os lançamentos das principais plataformas - PC, PlayStation 5, Xbox Series X e Nintendo Switch.
- Todos os meses, mais de 5 milhões de usuários passam por nossas páginas. São mais de 7 milhões de page views no site. Estamos presentes ainda nas redes sociais, com destaque para o nosso canal no YouTube, com mais de 1 milhão de inscritos. Cobrimos ainda os principais eventos nacionais e internacionais do segmento, incluindo CES, MWC, Computex, IFA, BGS, entre outros.
- site oficial: https://www.adrenaline.com.br/
- site rss: https://www.adrenaline.com.br/feed/

---

# 📊 Status do projeto

> [!NOTE]
> ☁️ Em produção na AWS

> [!TIP]
> 🔎 Qualquer feedback entrar em contato com os desenvolvedores

---

# 🚀 Resultado

> [!IMPORTANT]
> 🛰️ Projeto concluído

> [!CAUTION]
> ⛔ Após a apresentação o projeto será excluído da aws para não gerar custo

<div align="center">
 <a href="https://youtu.be/AidiFbGnn28" target="_blank" aria-label="Acessar o vídeo do projeto no YouTube">
 <img width=100% src="./assets/imagens/readme/youtube-logo.gif" alt="Logotipo do YouTube" /></a>

 <details>
  <summary>Descrição da Imagem</summary>
  Esta imagem contém o logotipo do YouTube em movimento, sugerindo que o usuário pode clicar para assistir ao vídeo do projeto. O logotipo está centralizado, e o GIF cria uma sensação de interatividade. Ao clicar na imagem, o usuário será redirecionado para o vídeo do projeto no YouTube.
</details>

</div>

---

<div align="left">
  <b><h1>🧱 Estrutura de arquivos/pastas</h1></b>
</div>

<div align="left">
	
```
/AdrenalineStreamAPI
│
├── /docs                            # Pasta para documentação do projeto.
│   └── /Passo a Passo.PDF           # Arquivo de documentação de como foi feito o Deploy da Aplicação na AWS com EC2, ECS, ECR e Docker.
|
├── /back-end                        # Pasta reservada para tudo do back-end da aplicação.
|   └── /src                         # Subpasta para o source da aplicação back-end.
|       └── /node_modules            # Subpasta que contém todas as dependências e bibliotecas externas instaladas para o projeto, gerenciadas pelo npm / yarn.
|       |   └── ...                  # Dependências e bibliotecas.
|       |
|       |── /node-aws-s3-integration # Pasta que contém todos os arquivos e scripts necessários para o funcionamento da API.
|       |   ├── /rotas               # Subpasta que contém o arquivo de rotas.
|       |   |   └── rss-api.js       # Arquivo que define as rotas da API relacionadas ao processamento e integração do RSS com o Amazon S3.
|       |   |
|       |   ├── /bucket-s3.js        # Arquivo que contém a lógica de integração com o serviço Amazon S3, responsável por upload do arquivo para o bucket.
|       |   └── /rss-parser.js       # Arquivo responsável por pegar as informações do URL do RSS e transcrever cada item.
|       │
|       ├── main.js                  # Arquivo principal do projeto que inicia a aplicação e integra os diferentes módulos e componentes do projeto.
|       ├── package-lock.json        # Arquivo autogerado que garante a integridade das versões exatas das dependências instaladas.
|       ├── package.json             # Arquivo que define as dependências do projeto, scripts de execução, e outras configurações relacionadas ao projeto npm.
|       ├── .dockerignore            # Arquivo que lista os arquivos e pastas que devem ser ignorados pelo Docker ao criar a imagem da aplicação.
|       ├── .env                     # Arquivo que contém variáveis de ambiente sensíveis da AWS e configurações utilizadas pela aplicação.
|       ├── build.bat                # Arquivo em formato de script de lote para Windows, usado para automatizar a construção do projeto e enviar para o ECR.
|       ├── compose.bat              # Arquivo em formato de script de lote para Windows, usado para automatizar a composição de contêineres Docker.
|       ├── docker-compose.yml       # Arquivo de configuração do Docker Compose, usado para definir e gerenciar múltiplos contêineres Docker.
|       ├── Dockerfile               # Arquivo que contém as instruções para criar a imagem Docker do projeto.
|       ├── login.bat                # Arquivo em formato de script de lote para Windows, usado para automatizar o processo de login na AWS.
|       └── yarn.lock                # Arquivo autogerado pelo yarn que bloqueia as versões exatas das dependências, similar ao package-lock.json, mas específico para o yarn.
|
├── /front-end                       # Diretório responsável por organizar os arquivos relacionados ao front-end.
│   ├── /content                     # Diretorio responsável por manter o CSS.
│   │   └── style.css                # Estilo do Site.
│   │
│   ├── /controllers                 # Arquivos de controladores responsáveis pela lógica de interação entre view e model.
│   │   └── feedController.js        # Controlador para manipular feed.
│   │
│   ├── /models                      # Arquivos de modelos que representam os dados/Objetos e DTOs do app.
│   │   └── cardModel.js             # modelo e construtor do Card.
│   │
│   ├── /utils                       # Auxiliares.
│   │   |── fetchUtil.js             # Função para fazer requisições de fetch.
│   │   └── dateFormatter.js         # Função para retornar data no formato correto.
│   │
│   └── index.html                   # Arquivo HTML principal do front-end.
|
├── /assets                          # Pasta que contém arquivos de mídia e outros recursos usados na aplicação.
│   └── /imagens                     # Subpasta específica para armazenar imagens utilizadas no projeto.
|       └── /readme                  # Subpasta que contém imagens utilizadas especificamente no README.
|           ├── compassuol.jpg       # Arquivo de imagem da CompassUOL, utilizado no README.
|           ├── logo_adrenaline.svg  # Arquivo de imagem do site escolhido Adrenaline, utilizado no README.
|           ├── youtube-logo.png     # Arquivo de imagem da logo do youtube, utilizado no README.
|           ├── sistema.svg          # Arquivo de imagem do diagrama de desenho do sistema, utilizado no README.
|           ├── sistema-en.svg       # Arquivo de imagem do diagrama de desenho do sistema em inglês, utilizado no README.
│           └── logo-projeto.gif     # Arquivo de imagem gif da logo do projeto.
|
├── README-EN.md                     # Arquivo para documentação do projeto em inglês.
├── README.md                        # Arquivo para documentação do projeto em português.
├── CODE_OF_CONDUCT.md               # Arquivo de documento que estabelece as diretrizes de conduta para a comunidade do projeto.
├── LICENSE                          # Arquivo de documento que descreve os termos da licença sob a qual o projeto é distribuído.
├── SECURITY.md                      # Arquivo de documento que aborda as práticas e políticas de segurança do projeto.
└── .gitignore                       # Arquivo para indicar ao Git quais arquivos/tipos de arquivos não devem ser rastreados.
```

</div>

---

# 📐 Desenho do sistema

```mermaid

graph TD;
    %% Projeto AdrenalineStream API
    subgraph AdrenalineStream API

        %% Fluxo de Deploy
        ECS[Amazon ECS Cluster] -->|Executa Containers| EC2[Amazon EC2 Instance]
        EC2 -->|Deploy Container| ECR[Amazon ECR Repositório Docker]
        ECR -->|Imagem Docker| BE[Back-end Server Container Node.js/Express]

        %% Instância EC2 e Containers
        subgraph EC2[Amazon EC2 Instance]
            VM[Virtual Machine]
            subgraph VM[Virtual Machine Docker]
                BE[Back-end Server Container Node.js/Express]
            end
        end

        %% Fluxo de dados após "Iniciar API"
        BE -->|Processa RSS e Salva JSON| S3[Amazon S3 Bucket JSON]
        HTML[HTML Site Estático no S3] -->|"Inicia API"| BE

        %% Fluxo de dados após "Pegar Dados"
        S3 -->|"Retorna JSON"| HTML
        HTML -->|"Busca JSON do S3"| S3
        HTML -->|Exibe dados JSON| U[Usuário]

        %% Usuário interagindo com o sistema
        U -->|"Clique: Iniciar API"| HTML
        U -->|"Clique: Pegar Dados"| HTML

    end

    %% Classes de estilo
    classDef aws fill:#FF9900,stroke:#232F3E,stroke-width:2px,color:white;
    classDef vm fill:#1EC9E8,stroke:#232F3E,stroke-width:2px;
    classDef app fill:#4CAF50,stroke:#232F3E,stroke-width:2px;
    classDef external fill:#333,stroke:#232F3E,stroke-width:2px;
    classDef user fill:#000000,stroke:#232F3E,stroke-width:2px,color:white;

    class U user;
    class HTML,BE,RSS app;
    class S3 aws;
    class VM vm;
    class EC2,S3,ECR,ECS aws;
    class VM vm;
    class RSS external;

```

</div>

> [!warning]
> 🚧 GitHub mobile não tem suporte para mermaid, segue abaixo o diagrama do desenho do sistema

![Fluxograma do sistema AWS, representando a interação entre serviços como ECS, EC2, S3, ECR, com o usuário interagindo com um site estático.](./assets/imagens/readme/sistema.svg)

<div align="left">

<details>
  <summary>Descrição da Imagem</summary>
  Este fluxograma descreve um sistema baseado na AWS:

- **Amazon ECS Cluster**: Gerencia a execução de containers.
- **Amazon EC2 Instance**: Hospeda uma máquina virtual que executa um ambiente Docker.
- **Virtual Machine Docker**: Contém um container chamado "Back-end Server Container" que utiliza Node.js/Express.
- **Back-end Server Container**:
  - Processa feeds RSS e salva os dados como JSON no Amazon S3.
  - Inicializa uma API que permite interações com o sistema.
- **Amazon ECR (Elastic Container Registry)**: Hospeda imagens Docker que são usadas para criar containers no EC2.
- **Amazon S3 Bucket JSON**: Armazena arquivos JSON gerados pelo processamento dos feeds RSS.
- **HTML Site Estático no S3**: Permite que o usuário veja os dados JSON e interaja com a API.
- **Usuário**: Interage com o sistema por meio do site estático no S3.

### Fluxo:

1. O container é implantado na instância EC2 a partir do Amazon ECR.
2. A aplicação no container processa feeds RSS e armazena os dados em JSON no Amazon S3.
3. O site estático no S3:
   - Exibe os dados JSON extraídos.
   - Oferece opções para que o usuário inicie a API ou realize novas consultas.
4. A API inicializada retorna dados JSON ao site para exibição ao usuário.

O diagrama utiliza um fundo cinza escuro, com elementos dispostos em caixas coloridas:

- Laranja para serviços AWS.
- Azul para containers e backend.
- Verde para o site estático e interações do usuário.
- Conexões e setas em cinza claro.

</details>

</div>

---

# 🏗️ Estrutura da Arquitetura e fluxo de interação

**1. Arquitetura**

**Amazon ECS:**

- **Cluster ECS:**
- - Gerencia contêineres Docker com base na imagem armazenada no ECR.
- **Instância EC2:**
- - Executa os contêineres no cluster ECS.
- - Comunica-se com o S3 para armazenar/recuperar arquivos.

**Amazon S3:**

- **Bucket 1 (Site Estático):**
- - Hospeda a interface HTML.
- - Configurado para acesso público.
- **Bucket 2 (JSON):**
- - Armazena os arquivos JSON gerados pela API.

**Amazon ECR:**

- Contém a imagem Docker do back-end.

**Usuário Final:**

- Interage com o site no S3.

**2. Fluxo de dados:**

- **Ação do Usuário: Iniciar API:**
  O usuário clica em "Iniciar API" na interface HTML, o que aciona uma solicitação para a API Node.js. Ao fazer isso, a URL do feed RSS é enviada para o endpoint correspondente. A API então processa o conteúdo do feed, converte os dados para o formato JSON e, em seguida, os armazena no bucket do S3.

- Função da API: A API processa o feed RSS fornecido e salva os dados extraídos em um arquivo JSON no bucket do S3.

Endpoint: GET `/transcribe-rss`

- Descrição: Este endpoint faz a transcrição do feed RSS a partir de uma URL especificada e envia o arquivo JSON gerado para o bucket S3.
- Parâmetros:
- - `url` (string): URL do feed RSS a ser processado.
    Exemplo de Requisição:

```shell
  GET '<URL>/transcribe-rss?url=https://www.adrenaline.com.br/feed/'
```

- **Ação do Usuário: Pegar Dados:**
  O usuário clica em "Pegar Dados" na interface HTML, o que aciona uma solicitação para buscar os dados JSON armazenados no bucket S3. A API recupera o arquivo JSON do S3 e retorna os dados extraídos do feed RSS, que são então exibidos na interface HTML.

Endpoint: GET `/rss-transcriptions/RSS-dados-coletados.json`

- Descrição: Este endpoint retorna o arquivo JSON armazenado no bucket S3, que contém os dados extraídos do feed RSS.
- Parâmetros:
- - `url` (string): URL do arquivo JSON armazenado no S3.
    Exemplo de Requisição:

```shell
  GET '<URL>/rss-transcriptions/RSS-dados-coletados.json'
```

- **Exemplo de Resposta:**
  A resposta da API será um JSON com os dados transcritos do feed RSS. O formato pode ser semelhante ao seguinte:

```json
{
  "title": "titulo da noticia de teste gravado",
  "description": "texto de descrição da noticia de teste",
  "pubDate": "Dia da semana | Mes | Ano | Horario",
  "...": "..."
}
```

---

# ⚔️ Tecnologias

As seguintes ferramentas foram utilizadas para desenvolver esse projeto:

<div align="center">

|                                                                                                                                             Ferramenta                                                                                                                                             |                                       Utilizada                                       |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------: |
|                                            <img align="center" alt="Windows" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg">[Sistema Windows](https://www.microsoft.com/pt-br/windows)                                             |                                  Sistema operacional                                  |
|                                        <img align="center" alt="Visual Studio Code" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg">[Visual Studio Code](https://code.visualstudio.com/)                                         |                                   Editor de código                                    |
|                                                          <img align="center" alt="Trello" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/trello/trello-original.svg">[Trello](https://trello.com/)                                                          |                             Organização geral de tarefas                              |
|                                                     <img align="center" alt="Postman" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-original.svg">[Postman](https://www.postman.com/)                                                      |                                     Teste de API                                      |
|                                                       <img align="center" alt="HTML" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg">[HTML](https://www.w3schools.com/html/)                                                       |                   Utilizado para estruturar a interface do usuário                    |
|                                                         <img align="center" alt="CSS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg">[CSS](https://www.w3schools.com/css/)                                                          |                              Utilizado para estilizações                              |
|                                             <img align="center" alt="JavaScript" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[JavaScript](https://www.w3schools.com/js/)                                             |                    Utilizado para manipulação do DOM e requisições                    |
|                                      <img align="center" alt="Fetch API" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[Fetch API](https://www.w3schools.com/js/js_api_fetch.asp)                                      |                       Utilizada para realizar requisições HTTP                        |
|                                              <img align="center" alt="Toastr" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[Toastr](https://github.com/CodeSeven/toastr)                                              |                  Biblioteca para exibição de notificações e alertas                   |
|                                                        <img align="center" alt="NodeJs" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg"/>[NodeJs](https://nodejs.org/pt)                                                         |                                    Criação da API                                     |
|                                                        <img align="center" alt="Docker" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg">[Docker](https://www.docker.com/)                                                        |                                Conteinerização da API                                 |
|                                           <img align="center" alt="AWS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg">[AWS](https://aws.amazon.com/pt/)                                            |                            Projeto hospedado na cloud AWS                             |
| <img align="center" alt="Linux" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg">[Linux](https://aws.amazon.com/pt/linux/?amazon-linux-whats-new.sort-by=item.additionalFields.postDateTime&amazon-linux-whats-new.sort-order=desc) |               Sistema operacional Amazon Linux utilizado na máquina EC2               |
|                                                                        <img align="center" alt="GitHub" src="https://img.shields.io/badge/github-000000.svg?&logo=github&logoColor=#181717">[ GitHub](https://github.com/)                                                                         |                  Plataforma de hospedagem de repositórios de código                   |
|                                                                      <img align="center" alt="Discord" src="https://img.shields.io/badge/Discord-000000.svg?&logo=discord&logoColor=#5865F2">[ Discord](https://discord.com/)                                                                      |                          Plataforma Utilizada para reuniões                           |
|                                                                              <img align="center" alt="Git" src="https://img.shields.io/badge/git-000000.svg?&logo=git&logoColor=#F05032">[ Git](https://git-scm.com/)                                                                              |                         Ferramenta de versionamento de código                         |
|                                                                  <img align="center" alt="Express" src="https://img.shields.io/badge/express-000000.svg?&logo=express&logoColor=#000000">[ Express](https://expressjs.com/pt-br/)                                                                  |                       Framework para aplicações web em Node.js                        |
|                                                               <img align="center" alt="Dotenv" src="https://img.shields.io/badge/dotenv-000000.svg?&logo=dotenv&logoColor=#ECD53F">[ Dotenv](https://www.dotenv.org/docs/quickstart)                                                               |          Usado para configurar e proteger variáveis sensíveis em aplicações           |
|                                                               <img align="center" alt="RSS-Parser" src="https://img.shields.io/badge/rss-000000.svg?&logo=rss&logoColor=#FFA500">[ RSS-Parser](https://github.com/rbren/rss-parser)                                                                | Biblioteca utilizada para ler e processar dados de feeds RSS a partir das requisições |
|                                                              <img align="center" alt="Amazon S3" src="https://img.shields.io/badge/amazons3-000000.svg?&logo=amazons3&logoColor=#569A31">[ Amazon S3](https://aws.amazon.com/pt/s3/)                                                               |                Utilizado para armazenar o arquivo JSON e a página HTML                |
|                                                            <img align="center" alt="Amazon EC2" src="https://img.shields.io/badge/amazonec2-000000.svg?&logo=amazonec2&logoColor=#FF9900">[ Amazon EC2](https://aws.amazon.com/pt/ec2/)                                                            |             Hospeda a máquina virtual onde o contêiner docker é executado             |
|                                                            <img align="center" alt="Amazon ECS" src="https://img.shields.io/badge/amazonecs-000000.svg?&logo=amazonecs&logoColor=#FF9900">[ Amazon ECS](https://aws.amazon.com/pt/ecs/)                                                            |                     Pega a imagem docker no ECR e envia para EC2                      |
|                                                                                                                                                ...                                                                                                                                                 |                                          ...                                          |

</div>

---

# 📜 Glossário

<div align="center">

Certos termos são usados ao longo do projeto AdrenalineStream API com significados consistentes ou convenções, segue abaixo alguns deles.

| Termo          | Descrição                                         |
| -------------- | ------------------------------------------------- |
| **AWS**        | Serviços Web da Amazon.                           |
| **API**        | Interface de Programação de Aplicações.           |
| **Amazon S3**  | Serviço de Armazenamento Simples da Amazon.       |
| **Amazon EC2** | Serviço de Computação Elástica da Amazon.         |
| **Amazon ECS** | Serviço de Containerização Elástica da Amazon.    |
| **Amazon ECR** | Serviço de Registro de Containerização da Amazon. |
| **JSON**       | Notação de Objetos JavaScript.                    |

</div>

---

# 📋 Referências

- [Como escrever um README incrível no seu Github](https://www.alura.com.br/artigos/escrever-bom-readme)
- [O que é Commit e como usar Commits Semânticos](https://blog.geekhunter.com.br/o-que-e-commit-e-como-usar-commits-semanticos/)
- [Padrões de commits](https://github.com/iuricode/padroes-de-commits)
- [Feed RSS: como atualizar seus leitores em tempo real](https://rockcontent.com/br/blog/o-que-e-feed-rss/)
- [Create an RSS Reader in Node](https://sabe.io/tutorials/rss-reader-node)
- [Uploading Files to Amazon S3 using Node.js: A Comprehensive Guide with Examples](https://alexcodes.medium.com/uploading-files-to-amazon-s3-using-node-js-a-comprehensive-guide-with-examples-6d300dfe90f8)

---

# 📝 Autores

<div align="center">
  <table>
    <tr>
      <td>
        <div align="center">
          <a href="https://github.com/BakMarino" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/177773601?v=4" width="115" alt="Imagem de perfil de Amanda Marino no GitHub">
          </a><br>
	  <a href="https://github.com/BakMarino" target="_blank">
            <img src="https://img.shields.io/badge/amanda%20marino-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge com o nome Amanda Marino">
          </a>
	  <a href="https://www.linkedin.com/in/amanda-marino-276130247/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Amanda%20Marino-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn de Amanda Marino">
          </a><br>
          <details>
            <summary>Descrição da Imagem</summary>
            Esta imagem mostra a foto de perfil de Amanda Marino no GitHub. O badge do github e outro badge do linkedin, e ao clicar na imagem ou nos badges, você será direcionado ao perfil.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/GsteXD" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/142363261?v=4" width="115" alt="Imagem de perfil de Gustavo Tsuru no GitHub">
          </a><br>
	 <a href="https://github.com/GsteXD" target="_blank">
            <img src="https://img.shields.io/badge/Gustavo%20Tsuru-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge com o nome Gustavo Tsuru">
          </a>
	 <a href="https://www.linkedin.com/in/gustavo-seiji-tsuru-endo-a55b60204/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Gustavo%20Tsuru-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn de Gustavo Tsuru">
          </a><br>
          <details>
            <summary>Descrição da Imagem</summary>
            Esta imagem mostra a foto de perfil de Gustavo Tsuru no GitHub. O badge do github e outro badge do linkedin, e ao clicar na imagem ou nos badges, você será direcionado ao perfil.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/NeemiasBorges" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/51499704?v=4" width="115" alt="Imagem de perfil de Neemias Borges no GitHub">
          </a><br>
	 <a href="https://github.com/NeemiasBorges" target="_blank">
            <img src="https://img.shields.io/badge/Neemias%20Borges-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge com o nome Neemias Borges">
          </a>
	  <a href="https://www.linkedin.com/in/neemias-borges/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Neemias%20Borges-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn de Neemias Borges">
          </a><br>
          <details>
            <summary>Descrição da Imagem</summary>
            Esta imagem mostra a foto de perfil de Neemias Borges no GitHub. O badge do github e outro badge do linkedin, e ao clicar na imagem ou nos badges, você será direcionado ao perfil.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/RamonCintas" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/94750000?v=4" width="115" alt="Imagem de perfil de Ramon Gomes no GitHub">
          </a><br>
	  <a href="https://github.com/RamonCintas" target="_blank">
            <img src="https://img.shields.io/badge/Ramon%20Gomes-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge com o nome Ramon Gomes">
          </a>
	  <a href="https://www.linkedin.com/in/ramon-cg/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Ramon%20Gomes-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn de Ramon Gomes">
          </a><br>
          <details>
            <summary>Descrição da Imagem</summary>
            Esta imagem mostra a foto de perfil de Ramon Gomes no GitHub. O badge do github e outro badge do linkedin, e ao clicar na imagem ou nos badges, você será direcionado ao perfil.
          </details>
        </div>
      </td>
    </tr>
  </table>
</div>

---

# ⚖️ Licença

<div align="center">

Copyright [© COMPASS.UOL TECNOLOGIA LTDA - 1996 - 2024 - Todos os direitos reservados](https://compass.uol/pt/home/).<br/><br/>
<img width=100% src="./assets/imagens/readme/compassuol.jpg"/>

</div>

<p align="right">(<a href="#readme-top">Voltar ao topo</a>)</p>

<div align="center">

<img  
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=36&pause=1000&center=true&width=1488&height=90&lines=OBS%3A;Em+conformidade+com+as+leis+de+prote%C3%A7%C3%A3o+de+dados%2C;N%C3%A3o+compartilhamos+nenhum+c%C3%B3digo+nem+informa%C3%A7%C3%B5es+cr%C3%ADticas%2C;Priorizamos+a+privacidade+e+seguran%C3%A7a%2C;Por+isso+arquivos+e+links+foram+removidos." 
    alt="Texto animado dizendo:
    'OBS: Em conformidade com as leis de proteção de dados, não compartilhamos nenhum código nem informações críticas, Priorizamos a privacidade e segurança, Por isso arquivos e links foram removidos.'"
/>

<img 
    width="100%" 
    src="./assets/imagens/readme/security.gif" 
    alt="GIF ilustrando que os dados estão protegidos."
  />

<details>
  <summary>Descrição da Imagem</summary>
  A imagem exibe um GIF ilustrando que os dados estão protegidos.
</details>

</div>
