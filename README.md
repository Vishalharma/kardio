# kardio

Teams need an independent view of service health when their primary monitoring stack is unavailable or incomplete. kardio checks configured endpoints and presents service status, availability, and recent health history in a web dashboard.

## Features

- Discover services deployed on Kubernetes and Marathon.
- Check manually configured REST endpoints and TCP ports.
- Display service status, availability, failures, and recent events.
- Send status-change alerts through email and Slack.
- Support active-passive high availability across two nodes.
- Restrict access through LDAP-based role-based access control.

## Installation

kardio is a Java application. Install Java and Maven, then build the project from source:

```bash
git clone https://github.com/your-org/kardio.git
cd kardio
mvn clean package
```

The packaged JAR is written to `target/`. Configure the application with the settings required for your environment before starting it.

## Usage

Start the packaged application on port 8080:

```bash
java -jar target/kardio-*.jar --server.port=8080
```

Open `http://localhost:8080` in a browser. Add the endpoints, environments, regions, alert recipients, and other settings required by your deployment through the application configuration and administration interface.

## License

kardio is licensed under the Apache License 2.0. This project is based on [tmobile/kardio](https://github.com/tmobile/kardio) and retains the original project's Apache-2.0 attribution and license terms.

