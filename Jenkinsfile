pipeline {

	agent {

		label {

			label "built-in"
			customWorkspace "/mnt/kkk
		}
	}
          
	
	stage('HTTP') {
   
		steps {
        
            sh "yum install httpd -y"
	    
        }
    }

               stage('ser') {
   
		steps {
        
            sh "service httpd start"
	    
        }
    }

	    stage('Copy HTML') {
    steps {
        sh 'cp -r index.html /var/www/html/'
	sh "chmod -R 777 /var/www/html/"    
    }
}

	     stage('restart') {
    steps {
        sh "service httpd restart"
    }
}

    }
}


	   

    
