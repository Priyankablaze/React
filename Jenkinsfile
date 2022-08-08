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
                sh "cd /var/www/jenkins-react-app/"
                sh "rm -rf /var/www/jenkins-react-app/*"
                sh "mkdir -p /var/www/jenkins-react-app/"
                sh "cp -r /var/lib/jenkins/workspace/React/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
