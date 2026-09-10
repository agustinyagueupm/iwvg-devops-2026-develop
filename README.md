## [Máster en Ingeniería Web por la Universidad Politécnica de Madrid (miw-upm)](http://miw.etsisi.upm.es)

## Ingeniería Web: Visión General (IWVG) DevOps

> Este proyecto es un apoyo docente de la asignatura. 

### Estado del código
[![CI iwvg-devops](https://github.com/miw-upm/iwvg-devops-2026/actions/workflows/ci.yml/badge.svg)](https://github.com/miw-upm/iwvg-devops-2026/actions/workflows/ci.yml)
[![Quality gate status](https://sonarcloud.io/api/project_badges/measure?project=miw-upm-github_iwvg-devops-2026&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=miw-upm-github_iwvg-devops-2026)
[![AWS](http://54.194.26.150:8080/system/version-badge)](http://54.194.26.150:8080/system) 

### Tecnologías necesarias
`Java` `Maven` `GitHub` `GitHub Actions` `Sonarcloud` `Slack` `Spring-Boot` `GitHub Packages` `Docker` `OpenAPI`

#### 1. Crear un proyecto (**0.5 pto**)
Crear un proyecto Maven llamado: **iwvg-devops-apellido-nombre**, versión **6.0.0**. Para ello se aporta **zip** de la
plantilla.
> Recordar editar el pom y cambiar el nombre del artefacto (artifactId).   
> Recordar cambiar el nombre de la  carpeta.   
> Importarlo desde IntelliJ.   
> Crear un repositorio en GitHub con el mensaje del primer comit: "Initial. Nombre Apellido"
> Crear las ramas **staging** a partir de **master** y **develop** a partir de **staging**.

#### 2. Preparar la gestión mediante Scrum (**0.5 pto**)
> Crear un proyecto de gestión en GitHub y prepararlo para la metodología de Scrum (columnas, etiquetas, hitos...).
> Crear las tareas siguientes tareas técnicas:
* 1️⃣: Integración continua con **GitHub Actions**. 
* 2️⃣: Análisis del código con **Sonarcloud**. Incluir **Badge** en README con **link** a la cuenta de Sonar.
* 3️⃣: Despliegue en **AWS**. Incluir **Badge** en README con **link** a la url donde está desplegado.

#### 3. Preparación del ecosistema (2.5 ptos)
   Se crearán las siguientes 3 historias (Technical) pero, excepcionalmente, se trabajarán solo con la ramas develop y staging. 
   Si se cometen errores, no pasa nada, se elimina el issue y se crea otro. 
   Si cometemos errores en los commits, no pasa nada, se toma nota y para la próxima vez 
   se hace bien, no intentar ni corregir y dar marcha atras. Al evaluar, solo se tiene en cuenta si se acaba haciendo bien la gestión, los errores de inicio no se tienen en cuenta siempre que se acabe haciendo bien.
>   A partir de ahora, en todos los commits, siempre se añade al final la coletilla del número de issue, por ejemplo: "mensaje commit. #1"

  - 1️⃣ Integración continua con GitHub Actions. Incluir Badge en README con link.
    - Poner issue In Progress. Rellenar issue adecuadamente: Assignees, Stimation, Type
    - Cuando se suba develop, asegurarse que en el issue aparece la referencia del commit, ya que tiene asociado la coletilla #???
    - Finalmente, cuando se finaliza, se pone el tiempo real consumido en horas con un decimal (por ejemplo: 0.3) y se cierra el issue. Fijarse que el issue se desplaza automaticamente a Done
    - Ser realistas, no pasa nada si la estimación con el tiempo real es muy diferente, sólo aprendemos para estimar mejor la próxima vez.
   
  - 2️⃣ Análisis del código con Sonarcloud. Incluir Badge en README con link a la cuenta de Sonar.
    - Se tiene que realizar en dos etapas, primero se conecta, y luego se establece rama por defecto y patrón de ramas.
   
  - 3️⃣ Deploy con AWS. Incluir Badge en README con link.
    - En CD probar primero Build & Push Docker image sin AWS. En este caso debe subirse la rama staging. Comprobar que se ha creado el docker en github packages
    - Crear instancia Lightsail (Ubuntu 22.04 LTS, 0.5GB, 2 vCPUs) para stagin.
    - Subir docker de DB. Se ha facilitado estableciendo un deploy de DB con la rama postgres. Comprobar en la consola de AWS que el docker se levanta bien.
    - Subir docker del api, mediante la rama staging, comprobar en AWS que el docker se levanta bien. Probar con el navegador: http://???.???.???.???:8080/system.
    - Añadir el link del badge
    - Para main es exactamente lo mismo, para ahorrar costes se ha comentado el deploy en cd-main. Subir main y comprobar que se genera el docker en packages

1️⃣, 2️⃣, 3️⃣ representa el orden temporal de desarrollo de los issues.