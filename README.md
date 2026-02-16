# API de Gestió de Tasques

[![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.java.net/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.2-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Maven](https://img.shields.io/badge/Maven-3.9-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)](https://maven.apache.org/)
[![DockerHub](https://img.shields.io/badge/Docker-tasklist--api-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/joapuiib/tasklist-api)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![Built with](https://img.shields.io/badge/Built_with-GitHub_Copilot-7B68EE?style=for-the-badge&logo=github-copilot&logoColor=white)](https://github.com/features/copilot)

## Descripció

Projecte d'exemple d'una API REST per a la gestió de tasques desenvolupat amb Java i Spring Boot. L'objectiu principal és demostrar la implementació de pipelines CI/CD i bones pràctiques de desenvolupament.

**Funcionalitats:**
- CRUD complet de tasques
- Filtrat per estat i cerca per títol
- Validació de dades
- Proves automatitzades

## Tecnologies

- **Java 21**
- **Spring Boot 3.2.2** (Spring Web, Spring Data JPA, Spring Validation)
- **H2 Database** (base de dades en memòria)
- **Maven** (gestió de dependències)
- **JUnit 5 + Mockito** (proves unitàries i d'integració)
- **Docker** (containerització)

## CI/CD - Fluxos de Treball

### Tests Automàtics
- **Flux de treball**: [`.github/workflows/tests.yml`](.github/workflows/tests.yml)
- **Trigger**: Pull Request a `develop` o `main`
- **Accions**:
  - Execució de tests unitaris (maven-surefire-plugin)
  - Execució de tests d'integració (maven-failsafe-plugin)
  - Publicació de resultats i informes en el PR
  - Bloqueig de merge si els tests fallen

### Construcció d'Imatge Docker (`docker-build.yml`)
- **Flux de treball**: [`.github/workflows/docker-build.yml`](.github/workflows/docker-build.yml)
- **Trigger**: Push de tag amb format `v*.*.*` (ex: `v1.0.0`)
- **Accions**:
  - Construcció de la imatge Docker
  - Publicació a Docker Hub
  - Etiquetatge semàntic (versió completa, major.minor, major, latest)


## Disclaimer
Aquest projecte ha sigut desenvolupat íntegrament utilitzant **GitHub Copilot** i **GitHub Copilot Agents**
i no es pot considerar com a un projecte real de producció ni pot ser servit com a referència per a pràctiques de desenvolupament reals.
El codi generat pot contenir errors, vulnerabilitats o pràctiques no recomanades que no han sigut revisades manualment.

El s'ha creat projecte només amb fins educatius i de demostració de com funcionen els fluxos
de treball amb GitHub Actions.
