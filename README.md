# DisasterReliefU-fund

A full-stack web application designed to facilitate disaster relief funding by connecting donors with specific needs during emergencies. The platform allows organizations to post disaster relief needs and enables users to contribute through a shopping cart-style donation system.

## Team
- Mary Almazan
- Emma Wheeler  
- Demitri Clark

## Prerequisites
- Java 21 (Make sure to have correct JAVA_HOME setup in your environment)
- Maven
- Angular

## How to run it

1. Clone the repository and go to the root directory.
2. In one terminal, go to the `ufund-api` directory, and execute:
   ```bash
   mvn compile exec:java
   ```
3. In a second terminal, go to the `ufund-ui` directory, and execute:
   ```bash
   # If it's your first time, run this first:
   npm install
   
   # Then start the development server:
   ng serve
   ```
4. Go to http://localhost:4200/
5. For admin features, enter "Admin" into login
6. For helper features, enter any other username.
7. Enjoy!

## Known bugs and disclaimers

(It may be the case that your implementation is not perfect.)

Document any known bug or nuisance. If any shortcomings, make clear what these are and where they are located.

## How to test it

The Maven build script provides hooks for run unit tests and generate code coverage reports in HTML.

### To run tests on all tiers together:
```bash
mvn clean test jacoco:report
```
Open in your browser the file at `PROJECT_API_HOME/target/site/jacoco/index.html`

### To run tests on a single tier:
```bash
mvn clean test-compile surefire:test@tier jacoco:report@tier
```
where `tier` is one of `controller`, `model`, `persistence`

Open in your browser the file at `PROJECT_API_HOME/target/site/jacoco/{controller, model, persistence}/index.html`

### To run tests on all the tiers in isolation:
```bash
mvn exec:exec@tests-and-coverage
```

**To view test results:**
- Controller tier tests: `PROJECT_API_HOME/target/site/jacoco/controller/index.html`
- Model tier tests: `PROJECT_API_HOME/target/site/jacoco/model/index.html`  
- Persistence tier tests: `PROJECT_API_HOME/target/site/jacoco/persistence/index.html`

*(Consider using `mvn clean verify` to attest you have reached the target threshold for coverage)*

## How to generate the Design documentation PDF

1. Access the `PROJECT_DOCS_HOME/` directory
2. Execute:
   ```bash
   mvn exec:exec@docs
   ```
3. The generated PDF will be in `PROJECT_DOCS_HOME/` directory

## How to setup/run/test program

1. Tester, first obtain the Acceptance Test plan
2. IP address of target machine running the app
3. Execute ________
   - ...
   - ...

## License

MIT License

See LICENSE for details.
