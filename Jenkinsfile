pipeline{
    agent any 
    stages{
        stage("Build")
        {
            steps{
                echo"Build the code using a build automation tool to compile and package your code."
                echo"Maven is a popular tool usd for the Java-based build automation that can handle dependency management, compilation, packaging, and testing"
                echo"Gradel can become useful is you eant to handel diverse languages."
            }
        }
        stage("Unit and Integration Tests")
        {
            steps{
                echo" Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected"
                echo"Jnit is the popular Java framework used for the purpose if intefration"
                echo"If you are looking for something for the web dev Selenium can be useful."
            }
        }
        stage("Code Analysis")
        {
            steps{
                echo" Integrate a code analysis tool to analyse the code and ensure it meets industry standards"
                echo"SonarQube can be useful in yhis case for continuous inspection of code qualoty and security."
            }
        }
        stage("Security Scan")
        {
            steps{
                echo"- Perform a security scan on the code using a tool to identify any vulnerabilities."
                echo"ZAP (Zed Attack Proxy) is a popular open-source web application security scanner."
            }
            post{
                success{
                    mail to: "artmania260@gmail.com",
                    subject: "Build Status Email",
                    body: "The file is safe to use."
                }
                failure{
                    mail to: "artmania260@gmail.com",
                    subject: "Build Status Email",
                    body: "Security issues found in the files presented."
                }
            }
        }
        stage("Deploy to Staging")
        {
            steps{
                echo"Deploy the application to a staging server"
                echo"Azure CLI is a command-line interface for Azure services, allowing to deploy to Azure infrastructure."
            }
        }
        stage("Integration Tests on Staging")
        {
            steps{
                echo"Run integration tests on the staging
                environment to ensure the application functions as expected in a production-likeenvironment."
                echo"Tools like JUnit and Selenium are again used after staging"
            }
            post{
                success{
                    mail to: "artmania260@gmail.com",
                    subject: "Build Status Email",
                    body: "Integration was successful."
                }
                failure{
                    mail to: "artmania260@gmail.com",
                    subject: "Build Status Email",
                    body: "Integration was uncusseful and something didn't work as expected."
                }
            }
        }
        stage("Deploy to Production")
        {
            steps{
                echo"Deploy the application to a production server"
                echo"Azure is also used in this stage. Aside from that AWS, ansible can also be used."
            }
        }

    }
}