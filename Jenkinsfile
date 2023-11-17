pipeline {
    agent any

    stages {
        stage('git') {
            
		steps {
                git 'https://github.com/ankushmohite/-repos.git'
            }
        }

          stage('HTTP') {
    steps {
        script {
            sh "yum install -y httpd"
	    sh "service httpd start"
        }
    }
}
               

	    stage('Copy HTML') {
    steps {
        sh 'sudo cp /root/.jenkins/workspace/gitpipe_master/index.html /var/www/html/'
    }
}

	     stage('restart') {
    steps {
        sh "service httpd restart"
    }
}

    }
}


	   

    
