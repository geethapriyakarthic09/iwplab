# Ex 08 - Aspect-Oriented Programming: Logging Method Execution

**Aim:** Use Spring AOP to log method name, arguments, return value and execution time without touching the business code.

**Files**
- `service/StudentService.java` - business methods (getStudentById, registerStudent)
- `aspect/LoggingAspect.java` - `@Aspect` class with `@Around` advice; pointcut `execution(* com.example.aopdemo.service.*.*(..))` = every method in the service package
- `controller/StudentController.java` - REST endpoints to trigger the service
- `pom.xml` - needs `spring-boot-starter-web` and `spring-boot-starter-aop`

**AOP terms (viva):** Aspect = logging class, Advice = the code that runs (`@Around`), Pointcut = which methods are intercepted, JoinPoint = the method being executed, `proceed()` = runs the real method.

**Run:** `mvn spring-boot:run`, then open `http://localhost:8080/students/101` and watch the console.
For the second method: `curl -X POST "http://localhost:8080/students/register?name=Raja"`

**Output:** see `output.txt` (add your console screenshot as `output.png`).

**Result:** Spring AOP successfully intercepts the service methods and logs their execution details. Logging (a cross-cutting concern) is kept separate from business logic.

**Note:** the manual's Result section mentions `@Before` and `@After`, but the code only uses `@Around`. `@Around` alone covers before + after, so this README says `@Around`.
