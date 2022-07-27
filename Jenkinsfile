pipeline {
    agent any 
    stages {
        stage('installing httpd') { 
            steps {

                sh "sudo rm -rvf /var/www/html/*"
                sh "sudo rm -rvf /var/www/html/.git"
                
            }
        }
        stage('Cloning repo') { 
            steps {
                sh "sudo git clone https://github.com/pemba3690/website.git /var/www/html/"
                // 
            }
        }
        stage('Reloading code') { 
            steps {
                sh "sudo systemctl reload httpd"
            }
        }
    }
}