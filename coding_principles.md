# Code quality and processes - DRAFT

As OCFs tech stack matures, we want to agree to some coding and processing standards. Below is a list of standards that we should try to maintain. There might be exceptions, but it gives us good guidelines. There are some other examples are here by [ibm](https://www.ibm.com/think/topics/code-quality), [Bytebtyego](https://bytebytego.com/guides/10-good-coding-principles-to-improve-code-quality/), [ramotion](https://www.ramotion.com/blog/what-is-code-quality/), [cisq](https://www.it-cisq.org/standards/code-quality-standards/), a [blog](https://blog.pixelfreestudio.com/ultimate-guide-to-code-quality-and-maintainability-in-2024/), and a [white paper from meta](https://arxiv.org/html/2504.12517v1).

## Contents
1. Code should be simple and understandable
2. Local development first
3. Testing is important
4. Every change should be reviewed
5. Data validation
6. Document how things work
7. Continuous improvement
8. Build it so it fails safely
9. Define clear boundaries
10.  Make the system observable
11. Make decisions as a team
12. Tech-on-call should do very little
13. Make production easy
14. AI tools are changing - fast

## Code

### 🧱 Code should be simple and understandable

Code should be easy to read, understandable and extendable. Prioritise maintainable, clear code that can be changed or expanded without unnecessarily breaking existing functionality. The less code we can have the better. Examples:
1. Variables and functions should be human readable so we can see what’s going on.
2. The code should explain itself, but sometimes we need to clarify the code with comments. Note that un-needed comments should be removed, and if there are a large amount of comments then we should think of refactoring that code.
3. If possible, let's try to use simple pure functions that are easier to understand than complicated classes.
4. Lets not have lots of embedded if statements as they can be make it hard to read and follow the logic.
5. Physical units confusions can lead to mistakes, lets include them when possible.
6. Code should use a linter and a formatter (we can use CI to check its linted and formatted properly) and we should use type hinting where possible.
7. Separation of concerns, e.g don't have a function that does X and Y, let’s have one function that does X, one function that does Y.
8. Frameworks like [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [SOLID](https://en.wikipedia.org/wiki/SOLID) are great to follow.

### 💻 Local development first

Run and test things locally as you develop. This helps improve the developer experience, reduces bugs, speeds up development cycles, and can help with debugging a problem. Examples:
1. Lets have a `Makefile` to run the application; `Make run` to run the application, `make lint`, `make format`, `make test`. We can also consider things like make `check-lint` to check the linting and `make clean` which cleans up any unneeded files.
2. Clear documentation of what environmental variables are needed, which are optional and what they do.
3. Centralised application configuration makes it clear what the application is doing. Lots of environmental variables throughout the code can be very hard to track down and difficult to understand. If possible load these at an application level, for example a config file which is easily read.
4. Have safe ways to interact with any infrastructure, for example have easy options like dry-run flags that might read from a database, but not save the results.

### ✅ Testing is important

Put significant emphasis on unit tests, supported by integration and end-to-end testing, to prevent regressions and maintain confidence in changes. Note that the test suite should be appropriate and improve the developer experience. Also note that the test suite should adhere to our code standards. Examples:
1. If you write a new function with new business logic in it, write a test for it and check the different expected behaviours. If this becomes complicated, you might want to divide your function up into small pieces.
2. Tests should be legible and should have good quality documentation.
3. Tests should be deterministic and external dependencies should be mocked when possible
4. For python libraries lets have one directory for all the tests
5. Keep test suite duration down, in order to speed up development lifecycle
6. Bonus you could use [TDD](https://en.wikipedia.org/wiki/Test-driven_development)

### 👀 Every change should be reviewed

High-quality PR reviews and CI: Code should be self-reviewed and reviewed by somewhere to check if the code is up to standard (as described in this document). CI is used for automated testing, linting, formatting and type checking to maintain code quality. Reviewers should ask questions and suggest changes when needed. Examples:
1. PRs should have good quality descriptions, this makes it easier for the reviewer and if anyone needs to subsequently look back at this PR.
2. PR should have a github issue linked to them - this helps give context about what this task was about and how it fits in with other bits of work.
3. All PRs should be reviewed by a person, and if its particular complicated a third person could help too.
4. AI code reviews are useful to catch simple thingsbut will still do a human review.
5. If we make a hot-fix PR we should make sure to label it as a hot-fix. Subsequent tidy/clean ups should be made into a github issue and linked with this PR. The github issue can then be prioritised.

### 🤝 Data validation

Strict data validation: Validate data properly/appropriately at clear boundaries rather than repeatedly throughout the application, with automated checks covering both inputs and outputs. Note that for multidimensional data this can be tricky, so high level checks should be done (like is the air temperature below 100 degrees)  Examples:
1. When reading satellite data that's going to be used for the forecast check for nans
2. When saving a forecast, check that is not zero during the day
3. Quick physical checks on NWP data, to check data is in the right range.

### 📄 Document how things work

Clear, up-to-date documentation: Maintain useful READMEs (see templates), documentation explaining how services work, how to run them, and how components fit together. Examples:
1. Clear instructions of how to run the service are really important, so it's easy for anyone to run them.
2. We are using microservices at OCF, so architecture diagrams are really important to show how the microservices typically interact.
3. There should be one source of truth, so we don't duplicate documentation.
4. Ensure knowledge is shared across the team so that people can understand, maintain and support systems without relying on one individual. One idea is to present results and share documentation.

### 🔄 Continuous improvement

Keep technical debt under control: Try to reduce technical debt as you go, if not allocate time to refactoring, reduce unnecessary complexity, and don't be afraid to rewrite or restructure code when the long-term result is worthwhile. Examples:
1. Periodically review tech debt and raise appropriately in technical planning sessions
2. If you see code that needs refactoring (but you don't have time now), make a github issue, and discuss with the team if this needs to be fixed now, or the next sprint (or later on)

## System

### 🦺 Build it so it fails safely

Fail fast, fail clearly, and fail gracefully. Never silently produce incorrect results or no results. Services should handle expected failures, protect downstream systems, and make problems obvious to the people operating them. Examples:
1. Individual service failures should not affect the whole system, for example if a forecast app run fails, we should still serve older forecasts to the users.
2. Services should gracefully degrade and remain operational when dependencies or inputs fail.
3. Specific example: The blend weights cannot be loaded and so no blend can be produced. Therefore the blend raises a failure immediately

### 🗝️ Define clear boundaries

Services and components should have clear responsibilities and contracts.
Define ownership, APIs, schemas and domain boundaries explicitly. Avoid unnecessary coupling between systems. Examples:
1. The data-platform with its database and API is a great example of clear boundaries that lots of microservices can use.
2. Common functional libraries like ocf-data-sampler should clearly define what they do and what structure the data is returned.

### 🚦 Make the system observable

We want clear observability and alerting. There should be useful logs and sensible automated alerts so the team can quickly understand what is happening and identify problems. Examples:
1. Logging should clear say whats happened (and sometimes what hasn't happened).
2. Logging should be searchable and should be minimal (so we don't have extra noise).
3. There should be clear alerting to the team to notify us of any critical failures.
4. Tools should be easily accessible to help understand the state of the system like the analysis-dashboard.
5. Trace IDs that can be passed to different microservices are very useful, so we can follow events through multiple microservices.

### 🫂 Make decisions as a team

Don't throw work over the fence. Involve the people who will build, operate, consume or depend on a system when designing it. Cross-functional collaboration should happen before problems reach production. Examples:
1. We might want to change the way ML experiments are saved, lets discuss as a team what the advantages and disadvantages of a new tools our, to help make a decision as a team together
2. We might want the NWP-consumer to start changing the format it saves data in. This should be discussed as a team as the forecast-app (and other microservices) uses this data and it should be discussed.
3. The solar capacity of a solar region can be defined in different ways. If we are changing this, let's make sure this is discussed as the forecast-app and APIs will use this data.

### 💆‍♂️ Tech-on-call should do very little

Simple, effective tech-on-call: The tech-on-call process should be easy to follow, automated where possible, and designed so that responders don't need extensive context to make decisions. Examples:
1. There should be clear notifications if anything is wrong
2. It should be very clear when/if to take action if there is a problem
3. Systems should be built robustly so there is automatic fail overs and automatic recover

### 🛠️ Make production easy

Deployments should be predictable, reversible and repeatable. Use environments that reasonably represent production, automate deployments where possible, and make it easy to promote, rollback and recover from failures. Examples:
1. If a microservice is upgraded but doesn't work as expected, we can roll back to the recent steady version.
2. Development and testing environments should closely reflect production, making it easier to identify problems before deploying to production and affecting critical users.

# Extras

### 14 AI tools are changing - fast

We have a AI policy [here](https://github.com/openclimatefix?q=github&type=all&language=&sort=#ai-policy) but AI tools are moving really fast. Our policy doesn't cover things like, should AI review all our PRs? We should keep reviewing this section and updating as appropriate. 
