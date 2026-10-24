# Ex 05 - Servlet-based Login System (GET and POST)

**Aim:** Develop a servlet-based login system that authenticates a user using GET and POST methods.

**How it works**
- `login.html` - form that sends username/password to `LoginServlet` using POST
- `doGet()` - displays the login form
- `doPost()` - reads the form values and checks them (admin / 12345); shows success or failure message
- `web.xml` - maps the servlet class to the URL `/LoginServlet`

**Folder layout (Eclipse Dynamic Web Project):**
```
src/LoginServlet.java
WebContent/login.html
WebContent/WEB-INF/web.xml
```

**Run**
1. Eclipse -> File -> New -> Dynamic Web Project (name it `LoginApp`)
2. Copy `LoginServlet.java` into `src`, `login.html` into `WebContent`, `web.xml` into `WebContent/WEB-INF`
3. Right click project -> Run As -> Run on Server (Apache Tomcat)
4. Open `http://localhost:8080/LoginApp/login.html`

**Note:** this uses `javax.servlet` so it needs **Tomcat 9 or lower**. For Tomcat 10+, change every `javax.servlet` to `jakarta.servlet` in the Java file and use the jakarta namespace in `web.xml`.

**Output:** see `output.txt` (add your screenshot).

**Result:** Thus, a Servlet-based login system was successfully developed to handle user authentication using GET and POST methods.
