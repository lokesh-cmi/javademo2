# javademo prototype

This is a microservice prototype generated using WeDAA, you can find documentation and help at [WeDAA Docs](https://www.wedaa.tech/docs/introduction/what-is-wedaa/)

## Prerequisites

- jdk version >= 17

## Project Structure

```
├── src/
    ├── main/
        ├── docker (contains docker compose files for external components based on architecture design)
        ├── java/javademo/
        └──  resources  (configuration properties)
    └── test/ (testcases for prototype)
        ├── java/javademo/
        └──  resources
├── target/
├── checkstyle.xml
├── comm.yo-rc.json (generator configuration file for communications)
├── mvnw
├── mvnw.cmd
├── package.json
├── pom.xml
├── README.md (Project documentation)
└── sonar-project.properties
```

## Get Started

The below cmd will install the required dependencies and run the prototype in local machine.

Run the prototype locally: `./mvnw`

Open [http://localhost:9083/management/health/readiness](http://localhost:9083/management/health/readiness) to view it in your browser.

You could see the below response in your browser:

```
{
  "status": "UP"
}
```

## Containerization

Docker image will be built with the prototype name.

- Build the docker image: `npm run java:docker`

Start the container: `docker run -d -p 9083:9083 javademo:latest`
