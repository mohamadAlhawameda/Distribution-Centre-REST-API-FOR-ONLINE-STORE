# Looking into the Distribution Centre

## Overview of the DC:  

The Distribution Centre (DC) application is a Spring Boot-based REST API designed to manage a distribution centre's inventory and user authentication. 

The application uses Spring Boot Starter modules, including Thymeleaf, Web, Data REST, Validation, Data JPA, and Security. It also uses an H2 in-memory database and Lombok for simplifying boilerplate code.




## Looking into the Models: 

There are three primary models in the DC

Distribution Centre 

Name (String)
Longitude (Integer)
Latitude (Integer)
Item(List<Item>)(One To Many Relationship)
 

## Item 

Name (String)
Brand (Enum)
YearOfCreation (Integer)
Price (BigDecimal)
Quantity (Integer)
Distribution Centre (ManyToOne relationship)


## User 

Username(String)
Password(String)

 

## Looking into the repositories Directory: 

The application consists of three repositories that extend CrudRepository for performing CRUD operations. 

a) DistributionCentreRepository

This manages the distribution centre entities. 

b) ItemRepository 

This manages the item entities  

c) UserRepository 

Manages User entities 
 
Provides a method to find a user by their username. 


Looking into the Entry Point Java File: 

DistributionCentreApplication class. This contains a main method that starts the Spring Boot Application 


Looking into the Data Loader: 

The CommandLineRunner bean in the entry point class loads initial data for the DistributionCentre, Item, and User entities. 
 
It saves two DistributionCentres, four items, and one User to the repositories
Looking into the Configuration: 

The application configuration is located in the application.properties, it specifies the H2 Database connection url and disables the generation of unique names for the in-memory database. 
 

Looking into the Build and Dependencies: 

The application is built using Maven, and the dependencies and build configuration are specified within the POM.xml file. 
 
Important dependencies include: Spring Boot Starter Modules, H2, DevTools, LomBok. 

In conclusion, the distribution centre application provides a basic REST API for managing distribution centre inventory and user authentication. 

It uses a combination of Spring Boot Modules and H2 in-memory database to deliver a functional and lightweight application. 



This now concludes the report for the distribution centre. 
