pipeline{
    agent any
    environment {
        root = "/usr/local/go/bin/go"
        branch = "master"
        scmUrl = "https://github.com/faisalramadhan673/simple-go-jenkins"
    }

    stages{
        stage("Git Clone"){
            steps {
                git branch: "${branch}", url: "${scmUrl}"
            }
        }

        stage("Dockerize"){
            steps {
                sh "docker build -t sample-jenkins ."
            }
        }

        stage("Deploy"){
            steps {
                echo "DEPLOY SUCCESS"
            }
        }
    }
}