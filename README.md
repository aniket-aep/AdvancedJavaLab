# Advanced Java Lab Projects - Java Swing Lab

A collection of Java Swing desktop applications developed as lab projects.

## Projects

### 1. Calculator

A simple calculator application built with **Java Swing** following the **MVC (Model-View-Controller)** architecture pattern.

#### Features

- Addition
- Subtraction
- Multiplication
- Division
- Percentage calculation

#### Architecture

```
Calculator/
├── Main.java       # Entry point
├── Cmodels.java    # Model - Business logic
├── Cviews.java     # View  - Swing UI components
└── Ccontroller.java# Controller - Event handling
```

#### How to Run

```bash
cd Calculator
javac *.java
java Calculator.Main
```

---

### 2. Registration Form

A desktop-based **student registration form** built with **Java Swing**.

#### Features

- Input fields: Name, Roll No, and Branch
- Gender selection using radio buttons (Male / Female)
- Terms & Conditions checkbox
- **Form validation** before submission
- Submit button with success popup
- Reset button to clear all fields

#### Validation Rules

- All text fields are required
- Gender must be selected
- Terms & Conditions must be accepted before submission

#### How to Run

```bash
cd "Registration Form"
javac aniket.java
java aniket
```

---

## Requirements

- Java Development Kit (JDK)

## License

MIT
