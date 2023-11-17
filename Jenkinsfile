pipeline{

        agent {
                label {
                        label "built-in"
                        customWorkspace "/mnt/app/"
                        }
                }

        stages {
               
		stage ("delete"){
			steps {
			sh "cd /mnt/app/"
			sh "rm -rf *"	
			} 
			}

		stage ("github repo") {
                        steps {
                           	git url:'https://github.com/HEMANT-111/pipe-jenkinsifle.git'
				
                                }
                        }

		stage ("copy_paste"){
			steps {
				sh "cp -r /mnt/app/index.html /var/www/html/ "
				sh "chmod -R 777 /var/www/html/ "
				sh "service httpd restart"
				}
			}
                }

}

	   

	   

    
