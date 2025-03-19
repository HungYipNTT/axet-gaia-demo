1. Generate DDL and testing data from a JPA Entity class:

```prompt
You are a Java developer working on a Spring Framework project

You are given a JPA Entity class
You will generate the DDL for create the table in Postgres DB
We also need the INSERT SQL to create 50 records for testing the search function, please make sure 50 statements are generated
The result should be in YAML format, it should only contain the DDL and INSERT SQL statements

JPA Entity class:"""
@Data
@Entity
public class Customer {
	
	@Id 
	private UUID id;

	@Max(value = 30)
	private String firstName;

	@Max(value = 30)
	private String lastName;

	@Max(value = 100)
	private String email;
	private String creditCard;

	@Max(value = 2)
	private String countryCode;

	@Max(value = 11)
	private String mobile;

	@Max(value = 50)
	private String address1;

	@Max(value = 50)
	private String address2;

	@Max(value = 50)
	private String address3;

	@Max(value = 50)
	private String address4;

	private String postCode;
	
}
""" 
```

1. Generate testing CURL commands from OpenAPI spec

```prompt
You are a QA response for testing the REST API

You are given a OpenAPI Spec for a Customer CRUD REST API 
You have to generate the curl commands for testing the API

OpenAPI Spec:~~~
openapi: 3.0.4
info:
  title: "Simple Customer CRUD API for demo"
  version: "1.0"
paths:
  /customers:
    get:
      summary: Get top N customers.
      responses:
        200:
          description: ""
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Customer'
    post:
      summary: Create a customer.
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Customer'
      responses:
        201:
          description: ""
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Customer'
  /customers/{id}:
    parameters:
    - name: id
      in: path
      required: true
      schema: {}
    get:
      summary: Get a customer by id
      responses:
        200:
          description: ""
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Customer'
    put:
      summary: Update a customer.
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Customer'
      responses:
        200:
          description: ""
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Customer'
    delete:
      summary: Delete a cat.
      responses:
        200:
          description: ""
          content:
            application/json:
              schema: {}
components:
  schemas:
    Customer:
      description: Type "Customer".
      type: object
      properties:
        id:
          type: string
          format: uuid
        firstName:
          type: string
          maxLength: 30
        lastName:
          type: string
          maxLength: 30
          example: "Tom"
        email:
          type: string
          format: email

~~~
```
