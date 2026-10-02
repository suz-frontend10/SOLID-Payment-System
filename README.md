# SOLID Payment System

## Overview

This project demonstrates the application of the **SOLID principles** in Java by designing a flexible and maintainable payment system.

The project starts with a simple payment implementation that handles different payment methods using conditional statements. As new payment methods are introduced, the original approach becomes harder to maintain.

The system is redesigned using SOLID principles to make it easier to extend and maintain without repeatedly modifying existing code.

## Problem Statement

A payment system needs to support multiple payment methods, such as:

- Credit Card
- UPI
- Cash
- PayPal
- Wallet

In the initial implementation, a single class handles payment processing and refunds using conditional statements.

As more payment methods are added, the class becomes increasingly difficult to maintain. Some payment methods may also have different capabilities, such as whether they support refunds.

The goal of this project is to redesign the system using SOLID principles to address these problems.

## Design Approach

The project explores two stages:

1. **Initial implementation:** A single payment class uses conditional statements to process payments and refunds.
2. **Redesigned implementation:** The payment system is structured around abstractions and separate responsibilities, making it easier to add new payment methods and handle different capabilities.

## SOLID Principles Applied

### 1. Single Responsibility Principle (SRP)

A class should have one primary responsibility.

Instead of having one large class responsible for processing every payment method and handling refunds, responsibilities are separated into focused classes.

**Benefit:** Changes to one payment method are less likely to affect unrelated payment methods.

### 2. Open/Closed Principle (OCP)

Software entities should be open for extension but closed for modification.

The payment system is designed so that new payment methods can be added through separate implementations rather than repeatedly changing a large payment-processing class.

**Benefit:** New payment methods can be introduced with fewer changes to existing code.

### 3. Liskov Substitution Principle (LSP)

Objects of a subtype should be usable wherever their base type is expected without breaking the program's behavior.

Payment methods may not all support the same operations. For example, cash payments may not support refunds.

The design should avoid forcing a payment method to implement behavior it cannot provide.

**Benefit:** Each payment implementation can be used according to the capabilities it actually supports.

### 4. Interface Segregation Principle (ISP)

Clients should not be forced to depend on methods they do not use.

Payment operations and refund operations can be represented separately so that payment methods only implement the capabilities they need.

**Benefit:** Interfaces remain focused, and classes avoid unnecessary methods.

### 5. Dependency Inversion Principle (DIP)

High-level modules should depend on abstractions rather than concrete implementations.

The payment system can depend on payment interfaces instead of directly depending on specific payment classes.

**Benefit:** Payment implementations can be changed or extended with less impact on the code that uses them.

## Key Concepts Demonstrated

- SOLID principles in object-oriented programming
- Interfaces and abstraction
- Separation of responsibilities
- Extensible payment methods
- Handling different payment capabilities
- Dependency inversion

## Project Structure

```text
SOLID-Payment-System/
├── Payment.java
├── CreditCard.java
├── UPI.java
├── Cash.java
├── PayPal.java
├── Wallet.java
└── README.md
```

*The structure above is illustrative. Adjust the filenames to match the actual files in the repository.*

## How to Run

### Prerequisites

- Java JDK installed
- VS Code, IntelliJ IDEA, or another Java IDE

### Run the project

1. Clone the repository:

```bash
git clone https://github.com/suz-frontend10/SOLID-Payment-System.git
```

2. Open the project folder in your IDE.

3. Compile the Java files:

```bash
javac *.java
```

4. Run the class containing the `main()` method:

```bash
java Client
```

If your entry-point class has a different name, use that class instead.

## Learning Outcomes

Through this project, I explored how to:

- Identify design problems in a tightly coupled payment system.
- Apply SOLID principles to improve code structure.
- Use interfaces to create flexible abstractions.
- Separate payment processing from refund capabilities.
- Design a system that is easier to extend and maintain.

## Technologies Used

- **Language:** Java
- **Concepts:** Object-Oriented Programming, SOLID Principles

## Project Purpose

This is a learning project focused on understanding and applying SOLID principles through a practical payment-system example. It is intended for educational purposes and does not process real payments.

---

**Author:** Susanna Hebzibah  
**Repository:** [SOLID-Payment-System](https://github.com/suz-frontend10/SOLID-Payment-System)
