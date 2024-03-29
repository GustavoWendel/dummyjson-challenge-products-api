﻿# dummyjson-challenge-products-api

## Products API

This Products API allows you to manage information about products. Key features include retrieving all products, searching for specific products, and fetching details of a product by ID.

### Technologies Used
#### Spring Boot 3.1.8: Rapid development framework for Java applications based on the Spring Framework.
#### Spring Cloud OpenFeign: Declarative communication client for HTTP services. Facilitates integration with external APIs.
#### Java 17: The latest version of the Java language, bringing performance improvements and enhanced features.
#### Springdoc OpenAPI 3.0: Library for automatic generation of API documentation based on Spring annotations.

### Key Resources
1. Get All Products
Endpoint: GET /api/products
Description: Returns a paginated list of products, allowing adjustments for skip and limit for pagination.
Query Parameters:
skip (optional): Defines the number of records to skip in the query (default: 0).
limit (optional): Defines the maximum number of records to be returned in the query (default: 30).
2. Get Product by ID
Endpoint: GET /api/products/{id}
Description: Returns details of a product based on the provided ID.
Path Parameters:
{id}: Unique ID of the product.
3. Search for Products
Endpoint: GET /api/products/search
Description: Performs a search for products based on a search term, allowing adjustments for skip and limit for pagination.
Query Parameters:
q (required): Search term for products.
skip (optional): Defines the number of records to skip in the query (default: 0).
limit (optional): Defines the maximum number of records to be returned in the query (default: 30).
Common Responses
200 OK: The request was successful. Details of the requested product or the list of products are returned.
400 Bad Request: The request has invalid or missing parameters.
404 Not Found: The requested resource was not found (e.g., product by ID does not exist).
500 Internal Server Error: An internal server error occurred during the processing of the request.

## Project Configuration
This project uses Spring Boot and Springdoc for API documentation. Swagger/OpenAPI configuration can be enabled in the Spring properties file with the following properties:
springdoc.api-docs.enabled=true
springdoc.swagger-ui.enabled=true

Additionally, unit tests using the Mockito framework were implemented to ensure the correct functionality of the application services.

