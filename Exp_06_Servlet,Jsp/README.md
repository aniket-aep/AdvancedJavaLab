# Experiment 6: Jakarta Servlets & JavaServer Pages (JSP)

## 📌 Overview
This experiment brings together **Jakarta EE 10 Web Technologies** using **Apache Maven**. It demonstrates the complete web application lifecycle:
1. **Jakarta Servlets**: Session tracking, HTTP request/response processing, security filters, and container lifecycle event listeners.
2. **JavaServer Pages (JSP)**: Converting static HTML forms into dynamic JSP pages, Expression Language (`${param.var}` / `${attribute}`), and MVC separation of concerns.

---

## 🏗️ Architecture & Component Flows

### Flow 1: Authentication & Session Management (Servlets)
```
     Web Browser                  Tomcat Container (Jakarta EE 10)
 ┌─────────────────┐         ┌────────────────────────────────────────────────────────┐
 │ index.html/jsp  │────────►│ AppListener: @WebListener                              │
 │  (Login Form)   │         │ (Logs contextInitialized / sessionCreated events)      │
 └─────────────────┘         ├────────────────────────────────────────────────────────┤
         │                   │ LoginServlet: @WebServlet("/login")                    │
         │  POST admin/1234  │ Validates credentials -> req.getSession()              │
         └──────────────────►│ session.setAttribute("username", "admin")              │
                             ├────────────────────────────────────────────────────────┤
                             │ AuthFilter: @WebFilter("/home")                        │
                             │ - Active session? ──► Chain through to HomeServlet     │
                             │ - Null / Invalid? ──► Redirect to index.jsp            │
                             ├────────────────────────────────────────────────────────┤
                             │ HomeServlet: @WebServlet("/home")                      │
                             │ Renders protected user dashboard with logout link      │
                             ├────────────────────────────────────────────────────────┤
                             │ LogoutServlet: @WebServlet("/logout")                  │
                             │ session.invalidate() -> Redirect back to login         │
                             └────────────────────────────────────────────────────────┘
```

### Flow 2: HTML-to-JSP Conversion & MVC Form Processing
```
 ┌─────────────────┐               ┌───────────────────┐               ┌─────────────────┐
 │   student.jsp   │  HTTP POST    │   HelloServlet    │  forward()    │   result.jsp    │
 │ (Dynamic Input) │──────────────►│ (Model/Controller)│──────────────►│ (View Rendering)│
 └─────────────────┘  form data    └───────────────────┘  data model   └─────────────────┘
                                     - req.getParameter()                - ${studentName}
                                     - Business validation               - ${rollNumber}
                                     - req.setAttribute()                - ${branch}
```

---

## 🗂️ Project Directory Structure

```
Exp_06_Servlet,Jsp/
├── README.md                                  # This documentation guide
└── servlet/                                   # Maven Web Application Project
    ├── pom.xml                                # Jakarta EE 10 (Servlet 6.1, JSP 4.1, JSTL 3.0)
    └── src/main/
        ├── java/com/servlet/
        │   ├── AppListener.java               # @WebListener: Context & Session Lifecycle
        │   ├── AuthFilter.java                # @WebFilter("/home"): Session guard filter
        │   ├── HelloServlet.java              # @WebServlet("/hello"): Form processor
        │   ├── HomeServlet.java               # @WebServlet("/home"): Protected welcome page
        │   ├── LoginServlet.java              # @WebServlet("/login"): Credential authenticator
        │   └── LogoutServlet.java             # @WebServlet("/logout"): Session terminator
        └── webapp/
            ├── WEB-INF/
            │   └── web.xml                    # Deployment descriptor
            ├── index.html                     # HTML Login Page
            ├── index.jsp                      # Dynamic JSP Login Page
            ├── student.jsp                    # Converted Dynamic Registration Form
            ├── result.jsp                     # EL Presentation View
            ├── result-jstl.jsp                # Advanced JSTL & Core Tags View
            ├── footer.jsp                     # Included JSP footer fragment
            └── style.css                      # Modern CSS styling
```

---

## 🚀 How to Build and Deploy

### Prerequisites
* **Java Development Kit (JDK)**: JDK 17 or higher.
* **Apache Maven**: 3.8+ installed and available on PATH (`mvn -version`).
* **Apache Tomcat**: Tomcat 11 available in `Exp_06_Apache_Tomcat/apache-tomcat-11.0.25`.

### Step 1: Build Web Archive (WAR) with Maven
Navigate to the Maven project directory and run package:

```bash
cd "Exp_06_Servlet,Jsp/servlet"
mvn clean package
```

Upon a successful build, the WAR file is generated at:
```
servlet/target/servlet.war
```

### Step 2: Deploy to Apache Tomcat 11
Copy the generated WAR file into Tomcat's `webapps` directory:

**Windows PowerShell:**
```powershell
Copy-Item "target\servlet.war" "..\..\Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\webapps\servlet.war" -Force
```

**Linux / macOS:**
```bash
cp target/servlet.war ../../Exp_06_Apache_Tomcat/apache-tomcat-11.0.25/webapps/servlet.war
```

### Step 3: Start Tomcat & Access Web Applications
Start Tomcat:
```cmd
cd ..\..\Exp_06_Apache_Tomcat\apache-tomcat-11.0.25\bin
startup.bat
```

Open your browser and navigate to:

| Application Feature | Browser URL | Credentials / Notes |
| :--- | :--- | :--- |
| **JSP Student Form** | `http://localhost:8080/servlet/student.jsp` | Submits to `/hello`, displays output in `result.jsp` |
| **Servlet Login Page** | `http://localhost:8080/servlet/index.jsp` | Username: `admin`, Password: `1234` |
| **Protected Dashboard** | `http://localhost:8080/servlet/home` | Protected by `AuthFilter` |
| **Logout Endpoint** | `http://localhost:8080/servlet/logout` | Invalidates session and returns to login |

---

## 💡 Key Concepts Covered
* **MVC Web Architecture**: Controller (`HelloServlet`) handles input and forwards data; View (`result.jsp`) handles presentation.
* **State & Session Tracking**: Maintaining user state across multiple HTTP requests using `HttpSession`.
* **Security Interception**: Pre-processing and post-processing requests via `Filter` and `FilterChain`.
* **Lifecycle Monitoring**: Responding to container initialization and session lifecycle using `ServletContextListener` and `HttpSessionListener`.
* **Expression Language (EL)**: Eliminating Java scriptlets (`<% %>`) in favor of clean declarative syntax (`${...}`).
