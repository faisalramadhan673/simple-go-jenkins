pipeline{
    agent any
    environment {
        root = "/usr/local/go/bin/go"
        branch = "master"
        scmUrl = "https://github.com/faisalramadhan673/simple-go-jenkins"
    }

    stages{
        stage('Docker') {
            agent { docker { image 'golang' } }

            steps {
                sh "docker images"
                sh "go version"
                sh "${root} version"
                git branch: "${branch}", url: "${scmUrl}"
                sh "${root} test ./... -cover"
                sh "${root} build ./..."
            }
        }

        // stage("Go Version"){
        //     steps {
        //         sh "${root} version" 
        //     }
        // }

        // stage("Git Clone"){
        //     steps {
        //         git branch: "${branch}", url: "${scmUrl}"
        //     }
        // }

        // stage("Go Test"){
        //     steps {
        //         sh "${root} test ./... -cover"
        //     }
        // }

        // stage("Go Build"){
        //     steps {
        //         sh "${root} build ./..."
        //     }
        // }
    }
}