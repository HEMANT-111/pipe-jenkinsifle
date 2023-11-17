pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ankushmohite/-repos.git'
            }
        }

          stage('Install HTTP') {
    steps {
        script {
            sh 'sudo yum install -y httpd'
        }
    }
}
               stage('Start Apache') {
    steps {
        script {
            sh 'sudo service httpd start'
        }
    }
}

	    stage('Copy HTML to Apache Directory') {
    steps {
        sh 'sudo cp index.html /var/www/html/'
    }
}

	    
	    stage('Restart Apache') {
    steps {
        sh 'sudo systemctl restart httpd'
    }
}



	   

    }
}

