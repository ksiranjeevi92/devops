pipeline{
    agent any
    tools{
        nodejs "my-nodejs"
    }
    stages{
        stage('Build'){
            steps{
                echo "Building..."
                sh "npm install"
            }
        }
        stage("Test"){
            steps{
                echo "Testing...."
                sh "npm run test"
            }
        }

        stage("Deploy"){
            steps{
                echo "Deployig..."
            }
        }
    }
    post{
        always{
            echo "Always..."
        }
        success{
            echo "Success..."
        }
        failure{
            echo "Failure..."
        }
        unstable{
            echo 'Unstable...'
        }
    }
}