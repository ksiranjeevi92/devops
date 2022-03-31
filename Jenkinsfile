def gv
pipeline{
    agent any
    tools{
        nodejs "my-nodejs"
    }
    stages{
        stage('init'){
            steps{
                script{

                    gv = load 'script.groovy'
                }
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
                script{
                    gv.deploy()
                }
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