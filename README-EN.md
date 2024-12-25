<a id="readme-top"></a>

<div align="right">
	<spam>Languages</spam>

[![Click to access the content in Portuguese](https://flagsapi.com/BR/flat/32.png)](README.md)
[![Click to access the content in English](https://flagsapi.com/US/flat/32.png)](README-EN.md)

</div>

# 🌐 Project slideshow

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=088df8&height=120&section=header"/>
<div align="center">

![This image contains a blue “play” icon in the center, indicating the start of a project slideshow. The background has geometric shapes in dark blue tones, with the text “Project slideshow” at the top. It guides the user to click and start the presentation.](./assets/imagens/readme/logo-projeto-en.gif)

  <details>
  <summary>Image description</summary>
  This image contains a blue “play” icon in the center, indicating the start of a project slideshow. The background has geometric shapes in dark blue tones, with the text “Project slideshow” at the top. It guides the user to click and start the presentation.
  </details>

</div>
<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=088df8&height=120&section=footer"/>

---

<details>
<summary>Click here to view the table of contents</summary>
<br/>

:small_blue_diamond: [🌐 Project slideshow](#-project-slideshow)

:small_blue_diamond: [💡 About the project](#-about-the-project)

:small_blue_diamond: [🌐About the chosen site](#-about-your-chosen-site)

:small_blue_diamond: [📊Project status](#-project-status)

:small_blue_diamond: [🚀 Result](#-result)

:small_blue_diamond: [🧱 File/folder structure](#-filefolder-structure)

:small_blue_diamond: [📐 System design](#-system-design)

:small_blue_diamond: [🏗️ Architecture-structure-and-interaction-flow](#%EF%B8%8F-architecture-structure-and-interaction-flow)

:small_blue_diamond: [⚔️ Technologies](#%EF%B8%8F-technologies)

:small_blue_diamond: [📜 Glossary](#-glossary)

:small_blue_diamond: [📋 References](#-references)

:small_blue_diamond: [📝 Authors](#--authors)

:small_blue_diamond: [⚖️ License](#%EF%B8%8F-license)

</details>

# 💡 About the project

⚡ The AdrenalineStream API project is a JavaScript/NodeJS API implemented in Docker on AWS to extract relevant information from a website with content in RSS format. This application saves the data in a JSON file inside an S3 bucket, and allows the saved content to be consulted via an HTML page hosted on the AWS cloud.

---

<div align="center">
<img width=50% src="./assets/imagens/readme/logo_adrenaline.svg"/>
</div>

# 🌐 About your chosen site

- With more than 20 years' experience, Adrenaline is now the largest hardware website in
  Brazil. Every day, we bring you news, articles and analysis on components such as video cards, motherboards, processors and notebooks. In addition, we specialize in the gaming market, covering the launches of the main platforms - PC, PlayStation 5, Xbox Series X and Nintendo Switch.
- Every month, more than 5 million users visit our pages. There are more than 7 million page views on the site. We are also present on social media, especially our YouTube channel, with over 1 million subscribers. We also cover the main national and international events in the segment, including CES, MWC, Computex, IFA, BGS, among others.
- official website: https://www.adrenaline.com.br/
- rss site: https://www.adrenaline.com.br/feed/

---

# 📊 Project status

> [!NOTE]
> ☁️ In production on AWS

> [!TIP]
> 🔎 Any feedback please contact the developers

---

# 🚀 Result

> [!IMPORTANT]
> 🛰️ Project completed

> [!CAUTION]
> ⛔ After submission, the project will be excluded from aws so as not to generate costs

<div align="center">
  <a href="https://youtu.be/AidiFbGnn28" target="_blank"><img width=100% src="./assets/imagens/readme/youtube-logo-en.gif" alt="YouTube logo" /></a>
  
  <details>
  <summary>Image Description</summary>
  This image contains the YouTube logo in motion, suggesting that the user can click to watch the project's video. The logo is centered, and the GIF creates a sense of interactivity. By clicking on the image, the user will be redirected to the project's video on YouTube.
  </details>

</div>

---

<div align="left">
<b><h1>🧱 File/folder structure</h1></b>
</div>

<div align="left">
 
```
/AdrenalineStreamAPI
│
|── /docs                             # Folder for project documentation.
│   └── /Step by Step.PDF             # Documentation file on how the Application was Deployed on AWS with EC2, ECS, ECR and Docker.
|
|── /back-end                         # Folder reserved for everything in the application's back-end.
|   └── /src                          # Subfolder for the source of the back-end application.
|       └── /node_modules             # Subfolder containing all the dependencies and external libraries installed for the project, managed by npm / yarn.
|        |  └── ...	              # Dependencies and libraries.
|        |
|        |── /node-aws-s3-integration # Folder containing all the files and scripts needed for the API to work.
|        |   |── /routes              # Subfolder containing the routes file.
|        |   |   └── rss-api.js       # File that defines the API routes related to RSS processing and integration with Amazon S3.
|        |   |
|        |   |── /bucket-s3.js        # File containing the integration logic with the Amazon S3 service, responsible for uploading the file to the bucket.
|        |   └── /rss-parser.js       # File responsible for taking the information from the RSS URL and transcribing each item.
|        |
|        |── main.js                  # Main project file that starts the application and integrates the different modules and components of the project.
|        |── package-lock.json        # Self-generated file that guarantees the integrity of the exact versions of the installed dependencies.
|        |── package.json             # File that defines the project dependencies, execution scripts, and other settings related to the npm project.
|        |── .dockerignore            # File that lists the files and folders that should be ignored by Docker when creating the application image.
|        |── .env                     # File containing sensitive AWS environment variables and settings used by the application.
|        |── build.bat                # File in Windows batch script format, used to automate the construction of the project and send it to the ECR.
|        |── compose.bat              # File in batch script format for Windows, used to automate the composition of Docker containers.
|        |── docker-compose.yml       # Docker Compose configuration file, used to define and manage multiple Docker containers.
|        |── Dockerfile               # File containing the instructions for creating the project's Docker image.
|        |── login.bat                # File in batch script format for Windows, used to automate the login process on AWS.
|        └── yarn.lock                # File autogenerated by yarn that locks the exact versions of dependencies, similar to package-lock.json, but specific to yarn.
|
|── /front-end                        # Directory responsible for organizing the files related to the front-end.
│ |── /content                        # Directory responsible for maintaining CSS.
│ │   └── style.css                   # Site style.
│ │
│ |── /controllers                    # Controller files responsible for the interaction logic between view and model.
│ │   └── feedController.js           # Controller for handling feeds.
│ │
│ |── /models                         # Model files that represent the app's data/Objects and DTOs.
│ │   └── cardModel.js                # Card model and builder.
│ │
│ |── /utils                          # Auxiliaries.
│ │   |── fetchUtil.js                # Function to make fetch requests.
│ │   └── dateFormatter.js            # Function to return date in correct format.
│ │
│ └── index.html                      # Main HTML file for the front-end.
|
|── /assets                           # Folder containing media files and other resources used in the application.
│   └── /images                       # Specific subfolder for storing images used in the project.
|       └── /readme                   # Subfolder containing images used specifically in README.
|           |── compassuol.jpg        # CompassUOL image file, used in README.
|           |── logo_adrenaline.svg   # Image file from the chosen Adrenaline site, used in the README.
|           ├── youtube-logo.png      # Image file of the youtube logo, used in the README.
|           ├── sistema.svg           # Image file of the system design diagram, used in the README.
|           ├── sistema-en.svg        # Image file of the system design diagram in English, used in the README.
│           └── logo-projecto.gif     # Project logo gif image file.
|
├── README-EN.md                      # File for project documentation in English.
├── README.md                         # File for project documentation in Portuguese.
├── CODE_OF_CONDUCT.md                # Document file that establishes the conduct guidelines for the project community.
├── LICENSE                           # Document file describing the terms of the license under which the project is distributed.
├── SECURITY.md                       # Document file that addresses the project's security practices and policies.
└── .gitignore                        # File to indicate to Git which files/types of files should not be tracked.
```

</div>

---

# 📐 System design

```mermaid

graph TD;
    %% Project AdrenalineStream API
    subgraph AdrenalineStream API

        %% Deployment Flow
        ECS[Amazon ECS Cluster] -->|Runs Containers| EC2[Amazon EC2 Instance]
        EC2 -->|Deploy Container| ECR[Amazon ECR Docker Repository]
        ECR -->|Docker Image| BE[Back-end Server Container Node.js/Express]

        %% EC2 Instance and Containers
        subgraph EC2[Amazon EC2 Instance]
            VM[Virtual Machine]
            subgraph VM[Virtual Machine Docker]
                BE[Back-end Server Container Node.js/Express]
            end
        end

        %% Data Flow after "Start API"
        BE -->|Processes RSS and Saves JSON| S3[Amazon S3 JSON Bucket]
        HTML[HTML Static Website on S3] -->|"Start API"| BE

        %% Data Flow after "Fetch Data"
        S3 -->|"Returns JSON"| HTML
        HTML -->|"Fetches JSON from S3"| S3
        HTML -->|Displays JSON data| U[User]

        %% User interacting with the system
        U -->|"Click: Start API"| HTML
        U -->|"Click: Fetch Data"| HTML

    end

    %% Style Definitions
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
> 🚧 GitHub mobile does not support mermaid, below is a diagram of the system design

![Flowchart of the AWS system, representing the interaction between services such as ECS, EC2, S3, ECR, with the user interacting with a static website](./assets/imagens/readme/sistema-en.svg)

<div align=“left”>

<details>
  <summary>Image Description</summary>
  This flowchart describes a system based on AWS:

- **Amazon ECS Cluster**: Manages the execution of containers.
- Amazon EC2 Instance\*\*: Hosts a virtual machine that runs a Docker environment.
- **Virtual Machine Docker**: Contains a container called “Back-end Server Container” that uses Node.js/Express.
- Back-end Server Container:
  - Processes RSS feeds and saves the data as JSON in Amazon S3.
  - Initializes an API that allows interactions with the system.
- Amazon ECR (Elastic Container Registry)\*\*: Hosts Docker images that are used to create containers on EC2.
- Amazon S3 Bucket JSON: Stores JSON files generated by processing RSS feeds.
- **HTML Static Site in S3**: Allows the user to view JSON data and interact with the API.
- User: Interacts with the system via the static site in S3.

### Flow:

1. The container is deployed on the EC2 instance from Amazon ECR.
2. The application in the container processes RSS feeds and stores the data in JSON on Amazon S3.
3. The static site on S3:
   - Displays the extracted JSON data.
   - It offers options for the user to start the API or make new queries.
4. The initialized API returns JSON data to the site for display to the user.

The diagram uses a dark grey background, with elements arranged in colored boxes:

- Orange for AWS services.
- Blue for containers and backend.
- Green for the static site and user interactions.
- Connections and arrows in light gray.

</details>

</div>

---

# 🏗️ Architecture structure and interaction flow

**1. Architecture**

**Amazon ECS:**

- **ECS Cluster:**
- - Manages Docker containers based on the image stored in the ECR.
- **EC2 instance:**
- - Runs the containers on the ECS cluster.
- - Communicates with S3 to store/retrieve files.

**Amazon S3:**

- **Bucket 1 (Static Site):**
- - Hosts the HTML interface.
- - Configured for public access.
- **Bucket 2 (JSON):**
- - Stores the JSON files generated by the API.

**Amazon ECR:**

- Contains the Docker image of the back-end.

**End User:**

- Interacts with the website in S3.

**2. Data flow:**

- **User Action: Start API:**
  The user clicks on “Start API” in the HTML interface, which triggers a request to the Node.js API. In doing so, the URL of the RSS feed is sent to the corresponding endpoint. The API then processes the content of the feed, converts the data into JSON format and then stores it in the S3 bucket.

- API function: The API processes the RSS feed provided and saves the extracted data in a JSON file in the S3 bucket.

Endpoint: GET `/transcribe-rss`

- Description: This endpoint transcribes the RSS feed from a specified URL and sends the generated JSON file to the S3 bucket.
- Parameters:
- - `url` (string): URL of the RSS feed to be processed.
    Request example:

```shell
  GET '<URL>/transcribe-rss?url=https://www.adrenaline.com.br/feed/'
```

- **User Action: Get Data:**
  The user clicks on “Fetch Data” in the HTML interface, which triggers a request to fetch the JSON data stored in the S3 bucket. The API retrieves the JSON file from S3 and returns the data extracted from the RSS feed, which is then displayed in the HTML interface.

Endpoint: GET `/rss-transcriptions/RSS-data-collected.json`

- Description: This endpoint returns the JSON file stored in the S3 bucket, which contains the data extracted from the RSS feed.
- Parameters:
- - `url` (string): URL of the JSON file stored in S3.
    Request example:

```shell
  GET '<URL>/rss-transcriptions/RSS-data-collected.json'
```

- **Sample Response**
  The API response will be a JSON with the data transcribed from the RSS feed. The format can be similar to the following:

```json
{
  "title": "title of the recorded test report",
  "description": "description text of the test report",
  "pubDate": "Weekday | Month | Year | Time",
  "...": "..."
}
```

---

# ⚔️ Technologies

The following tools were used to develop this project:

<div align="center">

|                                                                                                                                                Tool                                                                                                                                                |                             Utilized                              |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------: |
|                                             <img align="center" alt="Windows" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg">[Windows system](https://www.microsoft.com/pt-br/windows)                                             |                         Operating system                          |
|                                        <img align="center" alt="Visual Studio Code" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg">[Visual Studio Code](https://code.visualstudio.com/)                                         |                            Code editor                            |
|                                                          <img align="center" alt="Trello" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/trello/trello-original.svg">[Trello](https://trello.com/)                                                          |                     General task organization                     |
|                                                     <img align="center" alt="Postman" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-original.svg">[Postman](https://www.postman.com/)                                                      |                            API testing                            |
|                                                       <img align="center" alt="HTML" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg">[HTML](https://www.w3schools.com/html/)                                                       |               Used to structure the user interface                |
|                                                         <img align="center" alt="CSS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg">[CSS](https://www.w3schools.com/css/)                                                          |                         Used for styling                          |
|                                             <img align="center" alt="JavaScript" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[JavaScript](https://www.w3schools.com/js/)                                             |              Used for DOM manipulation and requests               |
|                                      <img align="center" alt="Fetch API" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[Fetch API](https://www.w3schools.com/js/js_api_fetch.asp)                                      |                    Used to make HTTP requests                     |
|                                              <img align="center" alt="Toastr" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">[Toastr](https://github.com/CodeSeven/toastr)                                              |          Library for displaying notifications and alerts          |
|                                                        <img align="center" alt="NodeJs" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg"/>[NodeJs](https://nodejs.org/pt)                                                         |                           API creation                            |
|                                                        <img align="center" alt="Docker" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg">[Docker](https://www.docker.com/)                                                        |                    Containerization of the API                    |
|                                           <img align="center" alt="AWS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg">[AWS](https://aws.amazon.com/pt/)                                            |                  Project hosted in the AWS cloud                  |
| <img align="center" alt="Linux" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg">[Linux](https://aws.amazon.com/pt/linux/?amazon-linux-whats-new.sort-by=item.additionalFields.postDateTime&amazon-linux-whats-new.sort-order=desc) |         Amazon Linux operating system used on EC2 machine         |
|                                                                        <img align="center" alt="GitHub" src="https://img.shields.io/badge/github-000000.svg?&logo=github&logoColor=#181717">[ GitHub](https://github.com/)                                                                         |              Platform for hosting code repositories               |
|                                                                      <img align="center" alt="Discord" src="https://img.shields.io/badge/Discord-000000.svg?&logo=discord&logoColor=#5865F2">[ Discord](https://discord.com/)                                                                      |                    Platform used for meetings                     |
|                                                                              <img align="center" alt="Git" src="https://img.shields.io/badge/git-000000.svg?&logo=git&logoColor=#F05032">[ Git](https://git-scm.com/)                                                                              |                       Code versioning tool                        |
|                                                                  <img align="center" alt="Express" src="https://img.shields.io/badge/express-000000.svg?&logo=express&logoColor=#000000">[ Express](https://expressjs.com/pt-br/)                                                                  |             Framework for web applications in Node.js             |
|                                                               <img align="center" alt="Dotenv" src="https://img.shields.io/badge/dotenv-000000.svg?&logo=dotenv&logoColor=#ECD53F">[ Dotenv](https://www.dotenv.org/docs/quickstart)                                                               | Used to configure and protect sensitive variables in applications |
|                                                               <img align="center" alt="RSS-Parser" src="https://img.shields.io/badge/rss-000000.svg?&logo=rss&logoColor=#FFA500">[ RSS-Parser](https://github.com/rbren/rss-parser)                                                                |   Library used to read and process RSS feed data from requests    |
|                                                              <img align="center" alt="Amazon S3" src="https://img.shields.io/badge/amazons3-000000.svg?&logo=amazons3&logoColor=#569A31">[ Amazon S3](https://aws.amazon.com/pt/s3/)                                                               |           Used to store the JSON file and the HTML page           |
|                                                            <img align="center" alt="Amazon EC2" src="https://img.shields.io/badge/amazonec2-000000.svg?&logo=amazonec2&logoColor=#FF9900">[ Amazon EC2](https://aws.amazon.com/pt/ec2/)                                                            |     Hosts the virtual machine where the docker container runs     |
|                                                            <img align="center" alt="Amazon ECS" src="https://img.shields.io/badge/amazonecs-000000.svg?&logo=amazonecs&logoColor=#FF9900">[ Amazon ECS](https://aws.amazon.com/pt/ecs/)                                                            |      Takes the docker image from the ECR and sends it to EC2      |
|                                                                                                                                                ...                                                                                                                                                 |                                ...                                |

</div>

---

# 📜 Glossary

<div align="center">

Certain terms are used throughout the AdrenalineStream API project with consistent meanings or conventions, below are some of them.

| Term           | Description                               |
| -------------- | ----------------------------------------- |
| **AWS**        | Amazon Web Services.                      |
| **API**        | Application Programming Interface.        |
| **Amazon S3**  | Amazon Simple Storage Service.            |
| **Amazon EC2** | Amazon Elastic Compute Service.           |
| **Amazon ECS** | Amazon Elastic Containerization Service.  |
| **Amazon ECR** | Amazon Containerization Registry Service. |
| **JSON**       | JavaScript Object Notation.               |

</div>

---

# 📋 References

- [Como escrever um README incrível no seu Github](https://www.alura.com.br/artigos/escrever-bom-readme)
- [O que é Commit e como usar Commits Semânticos](https://blog.geekhunter.com.br/o-que-e-commit-e-como-usar-commits-semanticos/)
- [Padrões de commits](https://github.com/iuricode/padroes-de-commits)
- [Feed RSS: como atualizar seus leitores em tempo real](https://rockcontent.com/br/blog/o-que-e-feed-rss/)
- [Create an RSS Reader in Node](https://sabe.io/tutorials/rss-reader-node)
- [Uploading Files to Amazon S3 using Node.js: A Comprehensive Guide with Examples](https://alexcodes.medium.com/uploading-files-to-amazon-s3-using-node-js-a-comprehensive-guide-with-examples-6d300dfe90f8)

---

# 📝 Authors

<div align="center">
  <table>
    <tr>
      <td>
        <div align="center">
          <a href="https://github.com/BakMarino" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/177773601?v=4" width="115" alt="Profile image of Amanda Marino on GitHub">
          </a><br>
	 <a href="https://github.com/BakMarino" target="_blank">
            <img src="https://img.shields.io/badge/amanda%20marino-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge with the name Amanda Marino">
          </a>
	  <a href="https://www.linkedin.com/in/amanda-marino-276130247/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Amanda%20Marino-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn the Amanda Marino">
          </a><br>
          <details>
            <summary>Image Description</summary>
            This image shows Amanda Marino's profile picture on GitHub. The github badge and another linkedin badge, and by clicking on the image or the badges, you will be directed to the profile.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/GsteXD" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/142363261?v=4" width="115" alt="Profile image of Gustavo Tsuru on GitHub">
          </a><br>
         <a href="https://github.com/GsteXD" target="_blank">
            <img src="https://img.shields.io/badge/Gustavo%20Tsuru-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge with the name Gustavo Tsuru">
          </a>
	  <a href="https://www.linkedin.com/in/gustavo-seiji-tsuru-endo-a55b60204/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Gustavo%20Tsuru-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn the Gustavo Tsuru">
          </a><br>
          <details>
            <summary>Image Description</summary>
            This image shows Gustavo Tsuru's profile picture on GitHub. The github badge and another linkedin badge, and by clicking on the image or the badges, you will be directed to the profile.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/NeemiasBorges" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/51499704?v=4" width="115" alt="Profile image of Neemias Borges on GitHub">
          </a><br>
	  <a href="https://github.com/NeemiasBorges" target="_blank">
            <img src="https://img.shields.io/badge/Neemias%20Borges-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge with the name Neemias Borges">
          </a>
	  <a href="https://www.linkedin.com/in/neemias-borges/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Neemias%20Borges-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn the Neemias Borges">
          </a><br>
          <details>
            <summary>Image Description</summary>
            This image shows Neemias Borges' profile picture on GitHub. The github badge and another linkedin badge, and by clicking on the image or the badges, you will be directed to the profile.
          </details>
        </div>
      </td>
      <td>
        <div align="center">
          <a href="https://github.com/RamonCintas" target="_blank">
            <img loading="lazy" src="https://avatars.githubusercontent.com/u/94750000?v=4" width="115" alt="Profile image of Ramon Gomes on GitHub">
          </a><br>
	  <a href="https://github.com/RamonCintas" target="_blank">
            <img src="https://img.shields.io/badge/Ramon%20Gomes-F6C953?style=for-the-badge&logo=phoenixframework&logoColor=%23FD4F00" alt="Badge with the name Ramon Gomes">
          </a>
	  <a href="https://www.linkedin.com/in/ramon-cg/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-Ramon%20Gomes-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn the Ramon Gomes">
          </a><br>
          <details>
            <summary>Image Description</summary>
            This image shows Ramon Gomes' profile picture on GitHub. The github badge and another linkedin badge, and by clicking on the image or the badges, you will be directed to the profile.
          </details>
        </div>
      </td>
    </tr>
  </table>
</div>

---

# ⚖️ License

<div align="center">

Copyright [© COMPASS.UOL TECNOLOGIA LTDA - 1996 - 2024 - Todos os direitos reservados](https://compass.uol/pt/home/).<br/><br/>
<img width=100% src="./assets/imagens/readme/compassuol.jpg"/>

</div>

<p align="right">(<a href="#readme-top">Back to top</a>)</p>

<div align="center">

<img  
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=36&pause=1000&center=true&width=1488&height=90&lines=NOTE%3A;In+compliance+with+data+protection+laws%2C;We+do+not+share+any+code+or+critical+information%2C;We+prioritize+privacy+and+security%2C;Therefore%2C+files+and+links+have+been+removed." 
    alt="Animated text saying:
    'NOTE: In compliance with data protection laws, we do not share any code or critical information, We prioritize privacy and security, Therefore, files and links have been removed.'"
/>

<img 
    width="100%" 
    src="./assets/imagens/readme/security-en.gif" 
    alt="GIF illustrating that data is protected."
  />

<details>
  <summary>Image Description</summary>
  The image shows a GIF illustrating that data is protected.
</details>

</div>
