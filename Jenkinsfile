pipeline {
    agent any 
    stages {
        stage('installing httpd') { 
            steps {

                sh "sudo rm -rvf /var/www/html/*"
                sh "sudo rm -rvf /var/www/html/.git"
                
            }
        }
        stage('Test') { 
            steps {
                sh "sudo git clone https://github.com/pemba3690/website.git /var/www/html/"
                // 
            }
        }
        stage('Deploy') { 
            steps {
                sh "sudo systemctl reload httpd"
            }
        }
    }
}