1. Generate DDL and testing data from a JPA Entity class:

```prompt
You are a Java developer working on a Spring Framework project

You are given a JPA Entity class
You will generate the DDL for create the table in Postgres DB
We also need the INSERT SQL to create 50 records for testing the search function, please do not skip that
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
