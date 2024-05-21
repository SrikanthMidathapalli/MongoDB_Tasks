# Project Use Case: Library Management System

## Overview
Create a Library Management System using MongoDB. The system should manage books, authors, members, and borrowing activities. It should be capable of handling CRUD operations efficiently and maintain relationships between entities.

## Requirements
Entities and Relationships

### Books
- Attributes: title, ISBN, authorId, category, publishedDate, copiesAvailable

### Authors
- Attributes: name, bio, nationality

### Members
- Attributes: name, membershipDate, email, borrowedBooks

### Borrowing Activities
- Attributes: memberId, bookId, borrowedDate, dueDate, returnDate

### Relationships
- Each book has one author, but an author can write multiple books (One-to-Many relationship).
- A member can borrow multiple books, and a book can be borrowed by multiple members over time (Many-to-Many relationship).

## Tasks
### Design the Schema
- Define the collections and their respective fields.
- Set up the appropriate relationships between collections using references (e.g., authorId in Books collection referring to _id in Authors collection).

### Create Indexes
- Create indexes to optimize queries. For example, create an index on ISBN for the Books collection and email for the Members collection.

### Perform CRUD Operations
- Implement CRUD operations for each collection:
  - Books: Add new books, update book details, delete books, and list all books.
  - Authors: Add new authors, update author details, delete authors, and list all authors.
  - Members: Add new members, update member details, delete members, and list all members.
  - Borrowing Activities: Record new borrowing activities, update return dates, and list all borrowing activities for a member.
