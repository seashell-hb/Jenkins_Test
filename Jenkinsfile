pipeline{
    agent any
    stages{
        stage("One"){
            steps{
                echo "========executing steps from stage One========"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}