pipeline{
    agent any
    environment{
        NAME = 'SIRAN'
        LASTNAME='JEEVI'
        secret=credentials("SECRET_TEXT")
    }
    stages{
        stage("Build"){
            steps{
                echo "Name is ${NAME}"
                sh "echo Name is $NAME"
            }
        }
        stage("Test"){
            when{
                expression{
                    BRANCH_NAME == 'main' || BRANCH_NAME == 'dev'
                }
            }
            steps{
                echo "Testing..."
            }

        }
        stage("Deploy"){
            steps{
                echo "Deploying...."
            }
        }
    }
    post{
        always{
            echo "Im run always"
        }
        success{
            echo "Build Success"
        }
        failure{
            echo "Build failed"
        }
        unstable{
            echo "Unstable build"
        }
    }
}