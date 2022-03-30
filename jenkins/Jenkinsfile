pipeleine{
    agent any
    environment{
        NAME = 'SIRAN'
        LASTNAME='JEEVI'
        secret=credentials("SECRET_TEXT")
    }
    stages{
        stage("build"){
            echo "Name is ${NAME}"
            echo 'Name id $NAME'
        }
        stage("Test"){
            when{
                expression{
                    BRANCH_NAME == 'main' || BRANCH_NAME == 'dev'
                }
            }

            echo "Testing..."

        }
        stage("Deploy"){
            echo "Deploying...."
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