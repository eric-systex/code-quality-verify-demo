node('master') {


    if (env.BRANCH_NAME == 'master' || env.BRANCH_NAME == 'dev' ) {
        stage("Build Docker Image"){
            echo "build docker image"
            echo "Only dev/master branch can build docker image"
        }

        if(env.BRANCH_NAME == 'dev'){
            stage("Deploy to test"){
                echo "branch dev to deploy to environment test"
            }

            stage("Integration test"){
                echo "test环境集成测试"
            }

        }

        if(env.BRANCH_NAME == 'master'){
            stage("Deploy to prod"){
                echo "branch master to deploy to environment prod"
            }

            stage("Health check"){
                echo "prod检查"
            }

        }
    }


}







