# Data Dictionary API

## Automated Field Mapping Documentation for Complex Systems

### About
This tool addresses a critical gap in our development process. Business Analysts (BAs) often have access to JSON property paths through UI inspection, but they lack complete backend field mappings required for data queries and API integration. 

By automatically generating an **Excel (or XML) sheet** with detailed mappings for over **100 collections**, this project eliminates up to **98% of developers' manual effort**—accelerating API integration and reducing dependency on developers for backend mapping details.

## Features
### What It Does
This API generates a comprehensive **Excel sheet (DataDictionary.xlsx)** documenting:
- **Database Schema**: Collection names, field mappings, MongoDB document structures
- **Java Model Metadata**: Class names, field types, JSON property paths
- **Integration Blueprints**: Relationship between API payloads (JSON) and database fields
- **Type Definitions**: Data types (including generics like `List<String>`) 
- **Annotation-Based Insights**: `@Document`, `@JsonProperty`, `@Id` usages

### Problem It Solves
In enterprise systems with **100+ domain collections**, Business Analysts and integration teams previously:
- Relied on developers to manually write field mapping docs for:
  - **Data querying** (MongoDB ↔ API payloads)
  - **Third-party API integrations**
  - **Reporting/analytics pipelines**
- **Wasted ~16 hours/week** waiting for mapping sheets
- Faced **versioning issues** with outdated Excel files

---

## Running Locally

### 1. Verify Java 17 Installation
```sh
java -version
```
If Java 17 is not installed, use the following commands:
```sh
sudo apt update
sudo apt install openjdk-17-jdk
```

### 2. Verify Maven Installation
```sh
mvn -version
```
If Maven is not installed, use:
```sh
sudo apt update
sudo apt install maven
```

### 3. Build the Project
```sh
mvn clean install
```

### 4. Run the Project
```sh
mvn spring-boot:run
```

---

## Running with Docker

### 1. Build the Project
```sh
mvn clean install
```

### 2. Build the Docker Image
```sh
sudo docker build -t data-dictionary .
```

### 3. Run the Docker Container
```sh
sudo docker run -p 8080:8080 data-dictionary
```

---

## Reference Sheet
[Google Sheets Reference](https://docs.google.com/spreadsheets/d/1yS8NcLeS-HnX3COVLwHX7Uyjbu4YgXHVPzUzlI_CUnQ/edit?gid=423316914)

![Reference Image](https://github.com/user-attachments/assets/8bffd0cb-828b-4617-a0f4-33f6b46e04e1)
