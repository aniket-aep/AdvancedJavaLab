# Experiment 6: Apache Tomcat 11 Web Application Server

## 📌 Overview
This experiment covers installing, configuring, and operating the **Apache Tomcat 11.0.25** Web Application Server. Apache Tomcat serves as the reference runtime container for **Jakarta Servlet 6.1**, **Jakarta Server Pages (JSP) 4.1**, and **Jakarta Expression Language (EL) 5.0** specifications under **Jakarta EE 10**.

---

## 🏗️ Tomcat Architecture & Directory Layout

```
Exp_06_Apache_Tomcat/
└── apache-tomcat-11.0.25/
    ├── bin/                   # Execution binaries, startup & shutdown scripts (catalina.bat/sh)
    ├── conf/                  # Core XML server configuration (server.xml, web.xml, tomcat-users.xml)
    ├── lib/                   # Container-level JAR dependencies (servlet-api.jar, jsp-api.jar, el-api.jar)
    ├── webapps/               # Web application deployment directory
    │   ├── ROOT/              # Default root context application
    │   └── studentform/       # Pre-configured Student Registration Web Application
    ├── temp/                  # Ephemeral JVM temporary files
    ├── logs/                  # Access logs and catalina server output logs
    └── work/                  # Compiled JSP servlets and session serialization scratch space
```

### Core Configuration Files
* **`conf/server.xml`**: Primary server topology, defining `<Server>`, `<Service>`, `<Connector port="8080">`, and `<Engine>`.
* **`conf/web.xml`**: Default container-wide servlet definitions, MIME type mappings, and default welcome file list (`index.html`, `index.jsp`).
* **`conf/tomcat-users.xml`**: Role and credential repository for Tomcat Manager and Host Manager web applications.
* **`conf/context.xml`**: Context configuration loaded into all web applications.

---

## 🌐 Pre-Deployed Application: Student Registration Form Webapp

A complete client-validated **Student Registration Form** is pre-configured and deployed inside:
```
apache-tomcat-11.0.25/webapps/studentform/index.html
```

### Features:
* Clean, responsive HTML5 layout with CSS styling.
* Client-side JavaScript form validation (`Full Name`, `Roll Number`, `Branch`, `Age`, `Gender`, `Hobbies`, `Address`).
* Accessible via HTTP browser request once Tomcat is running.

---

## 🚀 How to Start and Operate Apache Tomcat

### Prerequisites
* **Java Development Kit (JDK)**: JDK 17, 21, or 26 configured in `JAVA_HOME`.

### Step 1: Start Tomcat Server
Open a terminal in `Exp_06_Apache_Tomcat/apache-tomcat-11.0.25/bin`:

**Windows (Command Prompt / PowerShell):**
```cmd
cd Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\bin
startup.bat
```

**Linux / macOS:**
```bash
cd Exp_06_Apache_Tomcat/apache-tomcat-11.0.25/bin
chmod +x *.sh
./startup.sh
```

A new Tomcat console window will open displaying:
```
Server startup in [XXXX] milliseconds
```

### Step 2: Access in Web Browser
* **Tomcat Default Welcome Page**:
  ```
  http://localhost:8080/
  ```
* **Deployed Student Registration Webapp**:
  ```
  http://localhost:8080/studentform/
  ```

### Step 3: Shutdown Tomcat Server
When finished testing:

**Windows:**
```cmd
cd Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\bin
shutdown.bat
```

**Linux / macOS:**
```bash
./shutdown.sh
```

---

## 💡 Key Concepts Covered
* **Servlet Container Role**: Handling HTTP request dispatching, thread pooling, and web context lifecycle.
* **Webapp Deployment**: Deploying static assets and exploded directory structures under `webapps/`.
* **Environment Variables**: Interfacing with `JAVA_HOME` and `JRE_HOME` for JVM execution.
