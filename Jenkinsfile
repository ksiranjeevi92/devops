pipeline{
    agent any
    tools{
        nodejs "my-nodejs"
    }
    stages{
        stage('Clone'){
            steps{

                git 'https://github.com/ksiranjeevi92/devops.git'
            }
        }
    }

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