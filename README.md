# DisasterReliefU-fund
A full-stack web application designed to facilitate disaster relief funding by connecting donors with specific needs during emergencies. The platform allows organizations to post disaster relief needs and enables users to contribute through a shopping cart-style donation system.

Team
Mary Almazan
Emma Wheeler
Demitri Clark

Prerequisites
Java 21 (Make sure to have correct JAVA_HOME setup in your environment)
Maven
Angular
How to run it
Clone the repository and go to the root directory.
In one terminal, go to the ufund-api directory, and execute mvn compile exec:java
In a second, go to the ufund-ui directory, [if it's your first time, run npm install first] and execute ng serve
Go to http:/localhost:4200/
For admin features, enter Admin into login
For helper features, enter any other username.
Enjoy!

Known bugs and disclaimers
(It may be the case that your implementation is not perfect.)

Document any known bug or nuisance. If any shortcomings, make clear what these are and where they are located.

How to test it
The Maven build script provides hooks for run unit tests and generate code coverage reports in HTML.

To run tests on all tiers together do this:

Execute mvn clean test jacoco:report
Open in your browser the file at PROJECT_API_HOME/target/site/jacoco/index.html
To run tests on a single tier do this:

Execute mvn clean test-compile surefire:test@tier jacoco:report@tier where tier is one of controller, model, persistence
Open in your browser the file at PROJECT_API_HOME/target/site/jacoco/{controller, model, persistence}/index.html
To run tests on all the tiers in isolation do this:

Execute mvn exec:exec@tests-and-coverage
To view the Controller tier tests open in your browser the file at PROJECT_API_HOME/target/site/jacoco/model/index.html
To view the Model tier tests open in your browser the file at PROJECT_API_HOME/target/site/jacoco/model/index.html
To view the Persistence tier tests open in your browser the file at PROJECT_API_HOME/target/site/jacoco/model/index.html
*(Consider using mvn clean verify to attest you have reached the target threshold for coverage)

How to generate the Design documentation PDF
Access the PROJECT_DOCS_HOME/ directory
Execute mvn exec:exec@docs
The generated PDF will be in PROJECT_DOCS_HOME/ directory
How to setup/run/test program
Tester, first obtain the Acceptance Test plan
IP address of target machine running the app
Execute ________
...
...
License
MIT License

See LICENSE for details.
