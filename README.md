# ci.jenkinsfile
pipeline{
    agent{
        node{label "master"}
    }

    steges{
        stage("build"){
            steps{
                script{
                    mvnHome = tool "maven"
                    sh "${mvnHome}/bin/mvn -v"
                }
            }
        }
    }

}
