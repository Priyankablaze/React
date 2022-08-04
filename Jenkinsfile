pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
             steps {
                sh "sudo npm start"
                echo "Deploy Successfull"
            }
        }
    }
}
