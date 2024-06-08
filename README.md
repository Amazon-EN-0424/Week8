# 📚 Week 8

## 🔢 Enumerated Types in JPA

### Understanding Enumerated Types
- **What are Enumerated Types?**
  - Enumerated types are a special kind of data type used to define a set of named constants.
  - In JPA, the `@Enumerated` annotation is used to map an enum type to a database column.

### Mapping Enumerated Types with JPA
- **Default Mapping:**
  - By default, JPA maps enum types to their ordinal values (0, 1, 2, etc.) in the database.
  - This mapping is achieved using the `@Enumerated(EnumType.ORDINAL)` annotation.

- **String Mapping:**
  - JPA also supports mapping enum types to their string representations using the `@Enumerated(EnumType.STRING)` annotation.
  - This approach provides more readable and maintainable values in the database.

## 🌐 Embeddable Types in JPA

### Understanding Embeddable Types
- **What are Embeddable Types?**
  - Embeddable types are used to represent a composite value that is part of a larger entity.
  - They allow for the reuse of common attributes across multiple entities.
  - In JPA, the `@Embeddable` annotation is used to define an embeddable type.

### Using Embeddable Types with JPA
- **Defining an Embeddable Type:**
  - Create a class and annotate it with `@Embeddable`.
  - The class should contain the attributes that form the composite value.

- **Embedding the Type in an Entity:**
  - Use the `@Embedded` annotation in the entity class to include the embeddable type as a member variable.
  - The attributes of the embeddable type will be mapped to columns in the same table as the entity.

## 🎮 Game of Thrones: Relationships in JPA and MySQL

### 🐉 Thargaryens and Dragons: One-to-One Relationship
- **Objective:**
  - Implement a one-to-one relationship between Thargaryens and their dragons using JPA and MySQL.
  - Each Thargaryen can have only one dragon, and each dragon belongs to only one Thargaryen.

### 🏰 Characters and Houses: Many-to-One Relationship
- **Objective:**
  - Establish a many-to-one relationship between characters and their respective houses in the Game of Thrones universe.
  - Multiple characters can belong to the same house, but each character can only be associated with one house.

### 🧱 The Wall and the Night's Watch: One-to-Many Relationship
- **Objective:**
  - Implement a one-to-many relationship between the Wall and the Night's Watch characters in the Game of Thrones world.
  - The Wall can have many Night's Watch characters associated with it, but each Night's Watch character is assigned to only one section of the Wall.

### 🤝 Characters and Alliances: Many-to-Many Relationship
- **Objective:**
  - Demonstrate a many-to-many relationship between characters and alliances in the Game of Thrones universe.
  - Characters can be part of multiple alliances, and each alliance can have multiple characters associated with it.
  - Example: The "Brotherhood Without Banners" alliance can have characters like Beric Dondarrion, Thoros of Myr, and Sandor Clegane as members, while these characters can also be part of other alliances.

## 🎨 Practical Exercises

### Exercise 1: Planets and Moons in the Star Wars Universe
- **Task:** Create a JPA application that models the relationships between planets and their moons in the Star Wars universe using JPA and MySQL.
- **Instructions:**
  - Set up a new project with the necessary dependencies for JPA and MySQL.
  - Create entity classes for planets and moons.
  - Use appropriate JPA annotations to define the one-to-many relationship between planets and moons.
  - Configure the database connection properties.
  - Implement repository interfaces for planets and moons using Spring Data JPA.
  - Write unit tests to verify the correctness of the relationship and perform CRUD operations.

### Exercise 2: Starships and Crew Members in the Star Trek Universe
- **Task:** Develop a JPA application that represents the relationships between starships and their crew members in the Star Trek universe using JPA and MySQL.
- **Instructions:**
  - Set up a new project with the required dependencies for JPA and MySQL.
  - Create entity classes for starships and crew members.
  - Use appropriate JPA annotations to establish the many-to-many relationship between starships and crew members.
  - Configure the database connection properties.
  - Implement repository interfaces for starships and crew members using Spring Data JPA.
  - Write unit tests to verify the functionality of the relationship and perform CRUD operations.

### 💡 Discussion
- Discuss the benefits and use cases of different relationship types in database design.
- Explore the role of JPA annotations in mapping object-oriented relationships to relational databases.
- Share best practices for designing and implementing entity relationships in JPA applications.

## 🧩 Practical Project: Game of Thrones Character and House Management System

### Project Description
- Develop a character and house management system for the Game of Thrones universe using JPA and MySQL.
- The system should allow users to perform CRUD operations on characters and houses, manage their relationships, and utilize enumerated and embeddable types.

### Project Requirements
- Implement the necessary entity classes for characters, houses, dragons, the Wall, the Night's Watch, and alliances.
- Establish the appropriate relationships between entities using JPA annotations.
- Utilize enumerated types for character titles and house sigils.
- Incorporate embeddable types for character locations and house words.
- Implement unit tests to verify the functionality of the relationships, enumerated types, and embeddable types.

### 🚀 Implementation Steps
- Step 1: Set up a new project with the required dependencies for JPA and MySQL.
- Step 2: Design and create the entity classes for characters, houses, dragons, the Wall, the Night's Watch, and alliances.
- Step 3: Define the relationships between entities using JPA annotations (`@OneToOne`, `@ManyToOne`, `@OneToMany`, `@ManyToMany`).
- Step 4: Implement enumerated types for character titles and house sigils using the `@Enumerated` annotation.
- Step 5: Create embeddable type classes for character locations and house words and use the `@Embedded` annotation in the entity classes.
- Step 6: Implement repository interfaces for each entity using Spring Data JPA.
- Step 7: Write unit tests to verify the functionality of relationships, enumerated types, and embeddable types.


