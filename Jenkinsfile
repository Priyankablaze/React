pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm run build"
                sh "npm start"
            }
        }
        stage("Deploy") {
            steps {
                sh "rm -rf /var/www/jenkins-react-app"
                sh "cp -r /var/lib/jenkins/workspace/jenkins-react-app/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
