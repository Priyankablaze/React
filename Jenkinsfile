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
                sh "rm -rf /var/www/jenkins-react-app/*"
                sh "cd /var/www/jenkins-react-app/"
                sh "cp -r /var/lib/jenkins/workspace/React/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
