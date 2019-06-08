pipeline{
    agent any
    stages{
        stage("One"){
            steps{
                echo "This is step1"
            }
        }
        stage("Two"){
            steps{
                input("Do you want to proceed?")
            }
            
        }
        stage("Three"){
            when{
                not {
                    branch "master"
                }
            }
            steps {
                echo "This is not a master branch"
            }
        }
        stage("Four"){
            parallel {
                stage("Unit Test") {
                    steps {
                        echo "Running unit test..."
                    }
                }
                stage ("Integration Test") {
                    steps {
                        echo "Running Integration Test..."
                    }
                }
            }
        }

    }
    
}