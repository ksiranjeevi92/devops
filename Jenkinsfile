pipeline{
    agent any
    tools{
        nodejs "my-nodejs"
    }
    stages{
        stage('init'){
            steps{
                gv = import 'script.groovy'
            }
        }
        stage('Build'){
            steps{
                when{
                    expression{
                        BRANCH_NAME == 'main' || BRANCH_NAME == 'dev'
                    }
                }
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