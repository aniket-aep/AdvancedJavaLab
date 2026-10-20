# Advanced Java Laboratory & Capstone Project Repository

[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Jakarta EE](https://img.shields.io/badge/Jakarta%20EE-10-F80000?logo=jakartaee&logoColor=white)](https://jakarta.ee/)
[![Apache Tomcat](https://img.shields.io/badge/Apache%20Tomcat-11.0.25-F8DC75?logo=apachetomcat&logoColor=black)](https://tomcat.apache.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Apache Maven](https://img.shields.io/badge/Apache%20Maven-3.9%2B-C71A36?logo=apachemaven&logoColor=white)](https://maven.apache.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Welcome to the **Advanced Java Laboratory** repository. This repository contains the complete curriculum sequence of laboratory experiments, Apache Tomcat 11 web runtime container, and the enterprise capstone project (**ShopSphere**).

All experiment modules and the capstone project reside directly at the repository root, aligned with the laboratory curriculum sequence.

---

## 🗂️ Repository Directory Structure

```
AJL/
├── README.md                                          # Master repository documentation (this file)
├── .gitignore                                         # Git ignore rules for build artifacts & runtime logs
│
├── Exp_01_Student_Registration_Form/                  # Exp 1: Desktop Student Registration Form (Swing)
│   ├── aniket.java                                    # Swing GUI, validation & event handling
│   ├── aniket.class                                   # Compiled Java bytecode
│   └── README.md                                      # Experiment 1 detailed guide
│
├── Exp_02_Calculator/                                 # Exp 2: Swing Calculator with MVC Pattern
│   ├── Ccontroller.java                               # Controller (ActionListener event dispatch)
│   ├── Cmodels.java                                   # Model (Arithmetic business logic)
│   ├── Cviews.java                                    # View (Swing JFrame UI components)
│   ├── Main.java                                      # Main entry point
│   └── README.md                                      # Experiment 2 detailed guide
│
├── Exp_03_Mysql_Connect(JDBC)/                        # Exp 3: JDBC Database Connectivity
│   ├── jdbc/
│   │   ├── src/App.java                               # DriverManager, PreparedStatement CRUD
│   │   ├── lib/mysql-connector-j-26.7.0.jar           # MySQL Type-4 JDBC driver JAR
│   │   ├── bin/App.class                              # Compiled application bytecode
│   │   └── README.md                                  # JDBC workspace notes
│   └── README.md                                      # Experiment 3 detailed guide
│
├── Exp_04_Server_Client_Basics/                       # Exp 4: TCP Socket Programming
│   ├── server.java                                    # ServerSocket listening on port 5000
│   ├── client.java                                    # Socket client connecting over TCP
│   ├── server.class                                   # Compiled server bytecode
│   ├── client.class                                   # Compiled client bytecode
│   └── README.md                                      # Experiment 4 detailed guide
│
├── Exp_05_RMI/                                        # Exp 5: Java Remote Method Invocation
│   ├── Calculator.java                                # Remote interface (java.rmi.Remote)
│   ├── CalculatorImpl.java                            # Remote implementation (UnicastRemoteObject)
│   ├── Server.java                                    # RMI Server & Registry binding
│   ├── Client.java                                    # RMI Client remote invocation
│   └── README.md                                      # Experiment 5 detailed guide
│
├── Exp_06_Apache_Tomcat/                              # Exp 6: Apache Tomcat 11 Web Container
│   ├── apache-tomcat-11.0.25/                         # Apache Tomcat 11.0.25 installation
│   │   ├── bin/                                       # Startup & shutdown scripts (startup.bat/sh)
│   │   ├── conf/                                      # Server XML configurations (server.xml, web.xml)
│   │   ├── lib/                                       # Servlet 6.1 & JSP 4.1 container libraries
│   │   └── webapps/
│   │       ├── ROOT/                                  # Default root web application
│   │       ├── studentform/                           # Pre-deployed Student Form HTML/CSS/JS webapp
│   │       └── servlet.war                            # Pre-deployed Jakarta Servlet & JSP application
│   └── README.md                                      # Experiment 6 Tomcat administration guide
│
├── Exp_06_Servlet_Login_App/                          # Exp 6: Jakarta Servlet Login Application (Maven)
│   ├── servlet/
│   │   ├── pom.xml                                    # Maven build (Jakarta Servlet 6.1)
│   │   └── src/main/
│   │       ├── java/com/servlet/                      # AppListener, AuthFilter, Login, Logout, Hello, Home
│   │       └── webapp/                                # index.html, WEB-INF/web.xml
│   └── README.md                                      # Experiment 6 Servlet Login guide
│
├── Exp_07_JSP_Conversion/                             # Exp 7: Dynamic JSP Conversion & JSTL (Maven)
│   ├── servlet/
│   │   ├── pom.xml                                    # Maven build (Jakarta Servlet 6.1, JSP 4.1, JSTL 3.0)
│   │   └── src/main/
│   │       ├── java/com/servlet/                      # HelloServlet, AppListener, AuthFilter, Login, etc.
│   │       └── webapp/                                # student.jsp, result.jsp, result-jstl.jsp, footer.jsp, style.css
│   └── README.md                                      # Experiment 7 comprehensive JSP guide
│
└── ShopSphere/                                        # Major Capstone Project: Enterprise E-Commerce
    ├── pom.xml                                        # Master Maven project descriptor
    ├── README.md                                      # Complete ShopSphere developer guide
    ├── PROJECT_REPORT.md                              # Comprehensive academic project report
    ├── RTU_SYLLABUS_MAPPING.md                        # RTU Java syllabus curriculum mapping
    ├── database/shopsphere.sql                        # MySQL database schema & seed data
    ├── src/main/java/com/shopsphere/                  # Servlets, DAOs, Swing FlatLaf, Sockets, RMI
    └── src/main/webapp/                               # JSPs, Custom Tag Files, JSTL, CSS, JS
```

---

## 🔬 Laboratory Experiments Overview

### 1. Student Registration Form (Java Swing)
* **Directory**: [`Exp_01_Student_Registration_Form`](file:///c:/Users/anike/Downloads/AJL/Exp_01_Student_Registration_Form)
* **Concepts**: Java Swing GUI controls (`JFrame`, `JLabel`, `JTextField`, `JRadioButton`, `ButtonGroup`, `JCheckBox`), validation logic, `JOptionPane` modal dialogs, submit/reset event handling.
* **Run**:
  ```bash
  cd Exp_01_Student_Registration_Form
  javac aniket.java
  java aniket
  ```

---

### 2. Swing Calculator (MVC Architecture)
* **Directory**: [`Exp_02_Calculator`](file:///c:/Users/anike/Downloads/AJL/Exp_02_Calculator)
* **Concepts**: Model-View-Controller pattern, Swing GUI (`JFrame`, `JLabel`, `JTextField`, `JButton`), `ActionListener`, zero-division protection.
* **Run**:
  ```bash
  cd Exp_02_Calculator
  javac -d . *.java
  java Calculator.Main
  ```

---

### 3. MySQL Database Connectivity (JDBC)
* **Directory**: [`Exp_03_Mysql_Connect(JDBC)`](file:///c:/Users/anike/Downloads/AJL/Exp_03_Mysql_Connect(JDBC))
* **Concepts**: Type-4 JDBC driver (`com.mysql.cj.jdbc.Driver`), `DriverManager.getConnection()`, parameterized `PreparedStatement`, SQL injection prevention, DML execution on `college.student`.
* **Run**:
  ```bash
  cd "Exp_03_Mysql_Connect(JDBC)/jdbc"
  javac -cp "lib/mysql-connector-j-26.7.0.jar" -d bin src/App.java
  java  -cp "bin;lib/mysql-connector-j-26.7.0.jar" App
  ```

---

### 4. Server-Client Basics (TCP Sockets)
* **Directory**: [`Exp_04_Server_Client_Basics`](file:///c:/Users/anike/Downloads/AJL/Exp_04_Server_Client_Basics)
* **Concepts**: Stream sockets, `java.net.ServerSocket`, `java.net.Socket`, TCP handshake, buffered I/O stream communication on port `5000`.
* **Run** (using 2 terminals in `Exp_04_Server_Client_Basics`):
  ```bash
  javac server.java client.java
  java server              # Terminal 1: Starts Server
  java client              # Terminal 2: Connects Client -> Server: Hello Client
  ```

---

### 5. Java Remote Method Invocation (RMI)
* **Directory**: [`Exp_05_RMI`](file:///c:/Users/anike/Downloads/AJL/Exp_05_RMI)
* **Concepts**: Distributed computing, Remote Interface (`java.rmi.Remote`), `UnicastRemoteObject`, `rmiregistry` on port `1099`, `Naming.rebind()`, `Naming.lookup()`.
* **Run** (using 3 terminals in `Exp_05_RMI`):
  ```bash
  javac *.java
  start rmiregistry        # Terminal 1: Starts RMI Registry
  java Server              # Terminal 2: Starts RMI Server
  java Client              # Terminal 3: Executes Client -> Addition: 30 Subtraction: 10
  ```

---

### 6. Apache Tomcat 11 Web Application Server
* **Directory**: [`Exp_06_Apache_Tomcat`](file:///c:/Users/anike/Downloads/AJL/Exp_06_Apache_Tomcat)
* **Concepts**: Web application container topology, `webapps` deployment directory, `catalina` startup scripts, pre-configured `studentform` HTML5/CSS3/JavaScript webapp.
* **Run**:
  ```cmd
  cd Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\bin
  startup.bat
  ```
  Open browser at: `http://localhost:8080/studentform/`

---

### 6. Servlet Login Application (Jakarta EE & Maven)
* **Directory**: [`Exp_06_Servlet_Login_App`](file:///c:/Users/anike/Downloads/AJL/Exp_06_Servlet_Login_App)
* **Concepts**: Jakarta Servlet 6.1, Maven WAR packaging, session management (`HttpSession`), authentication security filter (`@WebFilter("/home")`), lifecycle listeners (`@WebListener`).
* **Run**:
  ```bash
  cd "Exp_06_Servlet_Login_App/servlet"
  mvn clean package
  ```
  Deploy `target/servlet.war` to Tomcat:
  ```powershell
  Copy-Item "target\servlet.war" "..\..\Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\webapps\servlet.war" -Force
  ```
  Start Tomcat and open: `http://localhost:8080/servlet/` (`admin` / `1234`).

---

### 7. Conversion of HTML into Dynamic JSP (Jakarta EE & Maven)
* **Directory**: [`Exp_07_JSP_Conversion`](file:///c:/Users/anike/Downloads/AJL/Exp_07_JSP_Conversion)
* **Concepts**: Converting static HTML to dynamic JSP (`student.jsp`), MVC dispatching (`forward`), Expression Language (EL: `${studentName}`), JSTL 3.0 Core/XML/SQL tags, modular JSP fragments (`footer.jsp`).
* **Build & Deploy**:
  ```bash
  cd "Exp_07_JSP_Conversion/servlet"
  mvn clean package
  ```
  Deploy the generated `target/servlet.war` to Tomcat:
  ```powershell
  Copy-Item "target\servlet.war" "..\..\Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\webapps\servlet.war" -Force
  ```
  Access via browser:
  * JSP Registration Form: `http://localhost:8080/servlet/student.jsp`
  * Dynamic JSP Login: `http://localhost:8080/servlet/index.jsp`

---

## 🌟 Major Capstone Project: ShopSphere

* **Directory**: [`ShopSphere`](file:///c:/Users/anike/Downloads/AJL/ShopSphere)
* **Documentation**:
  - [ShopSphere Developer Guide](file:///c:/Users/anike/Downloads/AJL/ShopSphere/README.md)
  - [Academic Project Report](file:///c:/Users/anike/Downloads/AJL/ShopSphere/PROJECT_REPORT.md)
  - [RTU Syllabus Curriculum Mapping](file:///c:/Users/anike/Downloads/AJL/ShopSphere/RTU_SYLLABUS_MAPPING.md)

### Key Capabilities
- **3-Tier Enterprise Web App**: Jakarta Servlets 6.0 + JSP 3.1 + JSTL 3.0 + Custom Tags (`<tags:productCard/>`, `<tags:rating/>`).
- **Modern Desktop Administration Console**: Java Swing MVC console with **FlatLaf Modern Look & Feel**, real-time product/order management, and sales metrics.
- **Distributed Networking**: Multi-threaded TCP inventory socket server (port 8088) with object serialization.
- **Distributed Objects**: Java RMI Remote Inventory Service on port 1099.
- **Dual Database Fallback**: Automated seamless fallback to **Embedded H2 In-Memory Database** if local MySQL is unconfigured, enabling 100% offline demonstrations.

### Execution Commands
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

## 📄 License
This repository is licensed under the [MIT License](LICENSE).
