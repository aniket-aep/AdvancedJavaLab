# Advanced Java Laboratory & Capstone Project Repository

[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Jakarta EE](https://img.shields.io/badge/Jakarta%20EE-10-F80000?logo=jakartaee&logoColor=white)](https://jakarta.ee/)
[![Apache Tomcat](https://img.shields.io/badge/Apache%20Tomcat-11.0.25-F8DC75?logo=apachetomcat&logoColor=black)](https://tomcat.apache.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Apache Maven](https://img.shields.io/badge/Apache%20Maven-3.9%2B-C71A36?logo=apachemaven&logoColor=white)](https://maven.apache.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Welcome to the **Advanced Java Laboratory** repository. This workspace contains the complete suite of **8 laboratory experiments**, the enterprise capstone project (**ShopSphere**), and local **software distributions** (Apache Tomcat 11 and MySQL Connector/J).

All experiment modules and the capstone project reside directly at the repository root for clean, immediate navigation.

---

## 🗂️ Repository Directory Structure

```
AJL/
├── README.md                                          # Master repository documentation (this file)
├── .gitignore                                         # Git ignore rules (protects Softwares, logs & binaries)
│
├── Exp-01-Calculator/                                 # Exp 1: Swing Calculator with MVC Pattern
│   ├── Ccontroller.java                               # Controller (ActionListener event dispatch)
│   ├── Cmodels.java                                   # Model (Arithmetic business logic)
│   ├── Cviews.java                                    # View (Swing JFrame UI components)
│   ├── Main.java                                      # Main entry point
│   └── README.md                                      # Experiment 1 detailed guide
│
├── Exp-02-Registration-Form/                          # Exp 2: Desktop Student Registration Form
│   ├── aniket.java                                    # Swing GUI, validation & event handling
│   └── README.md                                      # Experiment 2 detailed guide
│
├── Exp-03-RMI/                                        # Exp 3: Java Remote Method Invocation
│   ├── Calculator.java                                # Remote interface (java.rmi.Remote)
│   ├── CalculatorImpl.java                            # Remote implementation (UnicastRemoteObject)
│   ├── Server.java                                    # RMI Server & Registry binding
│   ├── Client.java                                    # RMI Client remote invocation
│   └── README.md                                      # Experiment 3 detailed guide
│
├── Exp-04-Server-Client-Basics/                       # Exp 4: TCP Socket Programming
│   ├── server.java                                    # ServerSocket listening on port 5000
│   ├── client.java                                    # Socket client connecting over TCP
│   └── README.md                                      # Experiment 4 detailed guide
│
├── Exp-05-MySQL-Connect/                              # Exp 5: JDBC Database Connectivity
│   ├── jdbc/
│   │   ├── src/App.java                               # DriverManager, PreparedStatement CRUD
│   │   └── lib/mysql-connector-j-26.7.0.jar           # MySQL Type-4 JDBC driver JAR
│   └── README.md                                      # Experiment 5 schema & execution guide
│
├── Exp-06-Student-Registration-Webapp/                # Exp 6: Web Student Registration Form
│   ├── index.html                                     # HTML5 form with CSS3 & JS validation
│   └── README.md                                      # Experiment 6 Tomcat deployment guide
│
├── Exp-07-Servlet-Login-App/                          # Exp 7: Jakarta Servlet Web App (Maven)
│   ├── servlet/
│   │   ├── pom.xml                                    # Maven dependencies (Jakarta Servlet 6.1)
│   │   └── src/                                       # Servlets, Filters, Listeners, index.html
│   └── README.md                                      # Experiment 7 architecture & deploy guide
│
├── Exp-08-JSP-Conversion/                             # Exp 8: HTML to Dynamic JSP & JSTL (Maven)
│   ├── servlet/
│   │   ├── pom.xml                                    # Maven build (JSTL 3.0, EL 5.0)
│   │   └── src/                                       # student.jsp, result.jsp, JSTL, Servlets
│   └── README.md                                      # Experiment 8 comprehensive guide
│
├── ShopSphere/                                        # Major Capstone Project: Enterprise E-Commerce
│   ├── pom.xml                                        # Master Maven project descriptor
│   ├── README.md                                      # Complete ShopSphere developer guide
│   ├── PROJECT_REPORT.md                              # Comprehensive academic project report
│   ├── RTU_SYLLABUS_MAPPING.md                        # RTU Java syllabus curriculum mapping
│   ├── database/shopsphere.sql                        # MySQL database schema & seed data
│   ├── src/main/java/com/shopsphere/                  # Servlets, DAOs, Swing FlatLaf, Sockets, RMI
│   └── src/main/webapp/                               # JSPs, Custom Tag Files, JSTL, CSS, JS
│
└── Softwares/                                         # Local Software Tools & Runtimes (Git Ignored)
    ├── README.md                                      # Software configuration & environment guide
    ├── apache-tomcat-11.0.25/                         # Apache Tomcat 11 Web Application Server
    └── mysql-connector-j-26.7.0/                      # MySQL Connector/J driver & source distribution
```

---

## 🔬 Laboratory Experiments (1 to 8)

Each experiment is self-contained with its source code and dedicated `README.md`.

### 1. Swing Calculator (MVC Pattern)
* **Directory**: [`Exp-01-Calculator`](file:///c:/Users/anike/Downloads/AJL/Exp-01-Calculator)
* **Concepts**: Model-View-Controller architecture, Swing GUI (`JFrame`, `JLabel`, `JTextField`, `JButton`), `ActionListener`, zero-division protection.
* **Run**:
  ```bash
  cd Exp-01-Calculator
  javac -d . *.java
  java Calculator.Main
  ```

---

### 2. Desktop Student Registration Form (Swing)
* **Directory**: [`Exp-02-Registration-Form`](file:///c:/Users/anike/Downloads/AJL/Exp-02-Registration-Form)
* **Concepts**: Swing GUI controls, `JRadioButton`, `ButtonGroup`, `JCheckBox`, form field validation, `JOptionPane` modal dialogs, submit/reset logic.
* **Run**:
  ```bash
  cd Exp-02-Registration-Form
  javac aniket.java
  java aniket
  ```

---

### 3. Remote Method Invocation (RMI)
* **Directory**: [`Exp-03-RMI`](file:///c:/Users/anike/Downloads/AJL/Exp-03-RMI)
* **Concepts**: Distributed computing, Remote Interface (`java.rmi.Remote`), `UnicastRemoteObject`, `rmiregistry` on port 1099, `Naming.rebind()`, `Naming.lookup()`.
* **Run** (using 3 terminals in `Exp-03-RMI`):
  ```bash
  javac *.java
  start rmiregistry        # Terminal 1: Starts RMI Registry
  java Server              # Terminal 2: Starts RMI Server
  java Client              # Terminal 3: Executes Client -> Addition: 30 Subtraction: 10
  ```

---

### 4. Server-Client Basics (TCP Sockets)
* **Directory**: [`Exp-04-Server-Client-Basics`](file:///c:/Users/anike/Downloads/AJL/Exp-04-Server-Client-Basics)
* **Concepts**: Stream sockets, `java.net.ServerSocket`, `java.net.Socket`, TCP handshake, buffered I/O stream communication on port 5000.
* **Run** (using 2 terminals in `Exp-04-Server-Client-Basics`):
  ```bash
  javac server.java client.java
  java server              # Terminal 1: Starts Server
  java client              # Terminal 2: Connects Client -> Server: Hello Client
  ```

---

### 5. MySQL Database Connectivity (JDBC)
* **Directory**: [`Exp-05-MySQL-Connect`](file:///c:/Users/anike/Downloads/AJL/Exp-05-MySQL-Connect)
* **Concepts**: Type-4 JDBC driver, `DriverManager.getConnection()`, parameterized `PreparedStatement`, SQL injection prevention, DML execution on `college.student`.
* **Run**:
  ```bash
  cd Exp-05-MySQL-Connect/jdbc
  javac -cp "lib/mysql-connector-j-26.7.0.jar" -d bin src/App.java
  java  -cp "bin;lib/mysql-connector-j-26.7.0.jar" App
  ```

---

### 6. Student Registration Form (Web Application & Tomcat)
* **Directory**: [`Exp-06-Student-Registration-Webapp`](file:///c:/Users/anike/Downloads/AJL/Exp-06-Student-Registration-Webapp)
* **Concepts**: Web application deployment structure, semantic HTML5, CSS3 responsive layout, client-side JavaScript form validation.
* **Run**:
  - Direct preview: Open `Exp-06-Student-Registration-Webapp/index.html` in your browser.
  - Deployed on Tomcat: Pre-configured in `Softwares/apache-tomcat-11.0.25/webapps/studentform/`. Start Tomcat and access: `http://localhost:8080/studentform/`.

---

### 7. Servlet Login Application (Jakarta EE & Maven)
* **Directory**: [`Exp-07-Servlet-Login-App`](file:///c:/Users/anike/Downloads/AJL/Exp-07-Servlet-Login-App)
* **Concepts**: Jakarta Servlet 6.1, Maven WAR packaging, session management (`HttpSession`), authentication security filter (`@WebFilter("/home")`), lifecycle listeners (`@WebListener`).
* **Run**:
  ```bash
  cd Exp-07-Servlet-Login-App/servlet
  mvn clean package
  copy target\servlet.war "..\..\Softwares\apache-tomcat-11.0.25\webapps\servlet.war"
  ```
  Start Tomcat and open: `http://localhost:8080/servlet/` (Credentials: `admin` / `1234`).

---

### 8. Conversion of HTML into Dynamic JSP (Jakarta EE & Maven)
* **Directory**: [`Exp-08-JSP-Conversion`](file:///c:/Users/anike/Downloads/AJL/Exp-08-JSP-Conversion)
* **Concepts**: Converting static HTML to dynamic JSP (`student.jsp`), MVC dispatching (`forward`), Expression Language (EL: `${name}`), JSTL 3.0 Core/XML/SQL tags, modular JSP fragments (`footer.jsp`).
* **Run**:
  ```bash
  cd Exp-08-JSP-Conversion/servlet
  mvn clean package
  copy target\servlet.war "..\..\Softwares\apache-tomcat-11.0.25\webapps\servlet.war"
  ```
  Open: `http://localhost:8080/servlet/student.jsp`

---

## 🌟 Major Capstone Project: ShopSphere

* **Directory**: [`ShopSphere`](file:///c:/Users/anike/Downloads/AJL/ShopSphere)
* **Documentation**:
  - [ShopSphere README](file:///c:/Users/anike/Downloads/AJL/ShopSphere/README.md)
  - [Complete Academic Project Report](file:///c:/Users/anike/Downloads/AJL/ShopSphere/PROJECT_REPORT.md)
  - [RTU Syllabus Curriculum Mapping](file:///c:/Users/anike/Downloads/AJL/ShopSphere/RTU_SYLLABUS_MAPPING.md)

### Key Capabilities
- **3-Tier Enterprise Web App**: Jakarta Servlets 6.0 + JSP 3.1 + JSTL 3.0 + Custom Tags (`<tags:productCard/>`, `<tags:rating/>`).
- **Modern Desktop Administration Console**: Java Swing MVC console with **FlatLaf Modern Look & Feel**, real-time product/order management, and sales metrics.
- **Distributed Networking**: Multi-threaded TCP inventory socket server (port 8088) with object serialization.
- **Distributed Objects**: Java RMI Remote Inventory Service on port 1099.
- **Dual Database Fallback**: Automated seamless fallback to **Embedded H2 In-Memory Database** if local MySQL is unconfigured, enabling 100% offline demonstrations.

### One-Click Execution Commands
```bash
cd ShopSphere

# 1. Start Embedded Web Application Server (Tomcat)
mvn exec:java
# URL: http://localhost:8080/shopsphere/
# Admin: admin@shopsphere.com / admin123 | Customer: customer@shopsphere.com / password123

# 2. Start Modern Swing Desktop Administration Console
mvn exec:java "-Dexec.mainClass=com.shopsphere.swing.SwingAdminLauncher"

# 3. Start Distributed TCP Socket Server & Client
mvn exec:java "-Dexec.mainClass=com.shopsphere.network.server.InventoryServer"  # Terminal 1
mvn exec:java "-Dexec.mainClass=com.shopsphere.network.client.InventoryClient"  # Terminal 2

# 4. Start Distributed RMI Server & Client
mvn exec:java "-Dexec.mainClass=com.shopsphere.rmi.server.RmiServer"            # Terminal 1
mvn exec:java "-Dexec.mainClass=com.shopsphere.rmi.client.RmiClient"            # Terminal 2
```

---

## 🛠️ Software & Setup Environments (Local Only)

All standalone servers and drivers required for local execution are housed inside [`Softwares/`](file:///c:/Users/anike/Downloads/AJL/Softwares) (configured in `.gitignore` so they are never pushed to GitHub):

1. **Apache Tomcat 11.0.25** (`Softwares/apache-tomcat-11.0.25`):
   - Start: `Softwares\apache-tomcat-11.0.25\bin\startup.bat`
   - Stop: `Softwares\apache-tomcat-11.0.25\bin\shutdown.bat`
   - Default Port: `8080` (`http://localhost:8080/`)
2. **MySQL Connector/J 26.7.0** (`Softwares/mysql-connector-j-26.7.0`):
   - Type-4 JDBC driver JAR: `Softwares/mysql-connector-j-26.7.0/mysql-connector-j-26.7.0.jar`

---

## 🔗 Git Configuration & Repository Status

| Attribute | Details |
| :--- | :--- |
| **Repository Remote (`origin`)** | `https://github.com/AniXDex/AdvancedJavaLab.git` |
| **Upstream Base Repository** | `https://github.com/aniket-aep/AdvancedJavaLab.git` |
| **Active Local Branch** | `main` |
| **Configured Git User** | `Aniket Saini` (`aniketxdop@gmail.com`) |

---

## 📄 License
This repository is licensed under the [MIT License](LICENSE).
