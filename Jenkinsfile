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
                sh "sudo rm -rf /var/www/html/jenkins-reactapp"
                sh "cd /var/www/html && mkdir jenkins-reactapp"
                sh "cd jenkins-reactapps"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/html/jenkins-reactapp/"
            }
        }
    }
}