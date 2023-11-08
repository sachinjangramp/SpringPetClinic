pipeline {
    agent any
    tools { 
        maven 'M1' 
        
    }
    stages{
        stage("Checkout"){
            steps {
                echo "Checkout"
                git url:"https://github.com/sachinjangramp/SpringPetClinic.git", branch:"main"
            }
        }
        stage("Clean"){
            steps{
                sh "mvn clean"
            }
        }
        stage("Validate"){
            steps{
                sh "mvn validate"
            }
        }
        stage("Compile"){
            steps{
                sh "mvn compile"
            }
        }
        stage("Test-Compile"){
            steps{
                sh "mvn test-compile"
            }
        }
        stage("Test"){
            steps{
                sh "mvn test"
            }
        }
        stage("Package"){
            steps{
                sh "mvn package"
            }
        }
        stage("Integration-Test"){
            steps{
                sh "mvn integration-test"
            }
        }
        stage("Verify"){
            steps{
                sh "mvn verify"
            }
        }
        stage("Install"){
            steps{
                sh "mvn install"
            }
        }
        stage("Deploy"){
            steps{
                sh "mvn deploy"
            }
        }
    }
}
