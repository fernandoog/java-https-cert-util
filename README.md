# Java HTTPS Certificate Utility

A console tool to automatically import HTTPS page certificates to Java certificate store.

## Description

This Spring Boot application allows you to easily import SSL certificates from HTTPS websites into your Java keystore. This is particularly useful when dealing with self-signed certificates or certificates not recognized by the default Java truststore.

## Features

- Automatically fetch and import certificates from HTTPS URLs
- Spring Boot-based console application
- Simple command-line interface
- Customizable keystore password

## Requirements

- Java 11 or higher
- Maven 3.x

## Installation

1. Clone this repository:
```bash
git clone https://github.com/fernandoog/java-https-cert-util.git
cd java-https-cert-util
```

2. Build the project:
```bash
mvn clean package
```

## Usage

### Using Maven

Run with Maven and provide the domain as an argument:

```bash
mvn spring-boot:run -Dspring-boot.run.arguments="google.es"
```

With custom keystore password:

```bash
mvn spring-boot:run -Dspring-boot.run.arguments="google.es password"
```

### Using JAR file

After building, run the JAR file:

```bash
java -jar target/java-https-cert-import-1.0.0.jar google.es
```

With custom keystore password:

```bash
java -jar target/java-https-cert-import-1.0.0.jar google.es password
```

## Examples

Import certificate for google.es:
```bash
mvn spring-boot:run -Dspring-boot.run.arguments="google.es"
```

Import certificate for a custom domain with password:
```bash
java -jar target/java-https-cert-import-1.0.0.jar example.com mypassword
```

## Troubleshooting

If you encounter issues with the keystore password, you can specify it as the second argument. The default password is typically `changeit`.

## Credits

This project is based on [InstallCert](https://github.com/escline/InstallCert) by escline.

## Author

Fernando Ortega Gorrita (@fernandoog)

## License

See LICENSE file for details.
