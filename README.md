# Cloud Non-Relational Databases in Action

A Spring Boot REST API for customer management that currently uses a local MongoDB database. The goal of this project
is to migrate it to use a **cloud MongoDB (Non-Relational Database Management System a.k.a NoSQL DBMS)** database service, transforming it into a
cloud-enabled application.

## About

This project is part of the **Enterprise Cloud Application (ECA)** module in the **Higher Diploma in Software
Engineering (HDSE)** program at the **Institute of Software Engineering (IJSE)**. It is intended exclusively for
students enrolled in this program.

## Objective

As it stands, this application stores all the data in the local MongoDB database server. Your task is to **clone this
repository** and migrate the data layer so that it uses a cloud non-relational MongoDB database (e.g., MongoDB Atlas,
AWS DocumentDB, Azure Cosmos DB for MongoDB), making the application fully cloud-enabled.

## Tech Stack

- **Java 25**
- **Spring Boot 4.1.0**
- **Spring Data REST** (auto-exposed RESTful APIs with HATEOAS)
- **Spring Data MongoDB**
- **Local/Public Cloud MongoDB**
- **Lombok**
- **Maven**

## API Endpoints

Spring Data REST automatically exposes the following HATEOAS-compliant endpoints:

| Method   | Endpoint                  | Description              |
|----------|---------------------------|--------------------------|
| `GET`    | `/api/v1/customers`       | Get a list of customers  |
| `GET`    | `/api/v1/customers/{id}`  | Get a customer by id     |
| `POST`   | `/api/v1/customers`       | Create a new customer    |
| `PATCH`  | `/api/v1/customers/{id}`  | Update a customer        |
| `DELETE` | `/api/v1/customers/{id}`  | Delete a customer by id  |

### Sample Request Body

```json
{
  "name": "John Doe",
  "address": "123 Main Street, Colombo"
}
```

## Getting Started

1. Clone the repository
2. Set up and connect the database
3. Build the project
   ```bash
   ./mvnw clean install
   ```
4. Run the application
   ```bash
   ./mvnw spring-boot:run
   ```
5. The application will start on the default port `8080` unless you have changed it. You can access the API endpoints using tools like Postman or cURL.

## Testing

A Postman collection is available for testing the API endpoints:

[Cloud Non-Relational Databases in Action - Postman Collection](https://www.postman.com/ijse-eca-5768309/workspace/eca-71-72/collection/47280517-e1ff2ba3-39ff-4337-ab79-33ac37d85d58?action=share&source=copy-link&creator=47280517)

## Need Help?

If you encounter any issues during the migration, feel free to reach out and start a discussion via the **Slack workspace**.