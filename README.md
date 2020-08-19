
# Tutorial: Creating a CRUD using Quarkus Java + REST + CDI + Panache, Hibernate with Postgres (Docker) + Postman
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://quarkus.io">
  </a>
  <h3 align="center">Quarkus IO</h3>
</p>

![List of Repositories](/assets/quarkus-logo.png)

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [Table of Contents](#tabela-de-conte%C3%BAdo)
- [About the project](#sobre-o-projeto)
  - [Done with](#feito-com)
- [Starting](#come%C3%A7ando)
  - [Prerequisites](#pr%C3%A9-requisitos)
  - [File Structure](#estrutura-de-arquivos)
  - [Installation](#instala%C3%A7%C3%A3o)
  - [Edition](#edi%C3%A7%C3%A3o)
  - [Publication](#publica%C3%A7%C3%A3o)
- [Contribution](#contribui%C3%A7%C3%A3o)
- [License](#licen%C3%A7a)
- [Contact](#contato)

<!-- ABOUT THE PROJECT -->

## About the project

Tutorial: Creating a CRUD using Quarkus Java + REST + CDI + Panache, Hibernate with Postgres (Docker) + Postman

### Done with

Technologies used in the project

- [JAVA] (https://www.java.com/pt_BR/download/) - Java is a programming language and computational platform first launched by Sun Microsystems in 1995. There are many applications and websites that will not work, unless you have Java installed, and more of these are created every day;

- [Quarkus] (https://quarkus.io/) - Red Hat released Quarkus, a native Kubernetes Java framework tailored for GraalVM and OpenJDK HotSpot. Quarkus aims to make java a leading platform in serverless and Kubernetes environments, offering developers a unified model of reactive and imperative programming;

<!-- GETTING STARTED -->

## Starting

To reproduce the example, it is necessary to follow the minimum requirements.

### Prerequisites

  - You will need an IDE such as: IntelliJ IDEA, Eclipse, VSCode.
  - Install JDK 8 or 11+
  - Install Apache Maven 3.5.3+ or Gradle
  - (Optional) - You can download GraalVM 19.2.1 to natively compile your application.
  - Panache Entity (Possible future article)

  #### Docker
  - Choose a client to connect to the database, example: DBeaver, PGAdmin, Postico (Mac)
  - Client to make REST requests: Postman or Insomnia.
  - Additional Instructions:
  - Docker installation (Official documentation)
  - Installing Docker on windows: (Youtube, ESR)
  - Installing Docker on Linux: (Youtube: LinuxTips)
  - Installing Docker on Mac: (Youtube: Wellington Rogati)

### File Structure

The file structure is as follows:

```bash
quarkus-food
├── README.md
├── pom.xml
├── quarkus-food.iml
└── src
    ├── main
    │   ├── docker
    │   │   ├── Dockerfile.jvm
    │   │   └── Dockerfile.native
    │   ├── java
    │   │   └── br
    │   │       └── com
    │   │           └── food
    │   │               ├── controller
    │   │               │   └── FoodController.java
    │   │               ├── entity
    │   │               │   └── Food.java
    │   │               └── resource
    │   │                   └── FoodResource.java
    │   └── resources
    │       ├── META-INF
    │       │   └── resources
    │       │       └── index.html
    │       └── application.properties
    └── test
        └── java
            └── br
                └── com
                    └── food
                        └── resource
                            ├── FoodResourceTest.java
                            └── NativeFoodResourceIT.java

19 directories, 12 files
```

### Application creation

1. To create the project, just use the Maven + Quarkus template, according to the command below:

`` sh
mvn io.quarkus: quarkus-maven-plugin: 1.0.1.Final: create \
      -DprojectGroupId = br.com.food \
      -DprojectArtifactId = quarkus-food \
      -DclassName = "br.com.food.resource.FoodResource" \
      -Dpath = "/ food"
``

(Alternative) - Quarkus offers a website called `Quarkus.code.io`, where it is possible to configure the project in a more visual way, it is worth checking out, follow the link: https://code.quarkus.io/

---

#### Running the Postgresql Instance in Docker

To start Postgresql, simply run the command below (Docker must be installed):

`` sh
docker run --name postgres-food -e "POSTGRES_PASSWORD = postgres" -p 5433: 5432 -v ~ / developer / PostgreSQL: / var / lib / postgresql / data -d postgres
``

### Executing the project in Quarkus

To run a project in Quarkus, just run the command:
`` sh
mvn compile quarkus: dev
``

<!-- CONTRIBUTING -->

## Contribution

Feel free to contribute to the project.

1. Fork the project
2. Create a Branch for your Feature (`git checkout -b feature / newFeature`)
3. Add your changes (`git add .`)
4. Commit your changes (`git commit -m 'New functionality to make it easier ...`)
5. Push the Branch (`git push origin feature / newFeature`)
6. Open a Pull Request

<! - LICENSE ->

## License

Distributed under the MIT license. See `LICENSE` for more information.

<!-- CONTACT -->

## Contato

Wilbur - 
[Github](https://github.com/jhowilbur)
[lindekin](https://www.linkedin.com/in/wilbur-dev/)
