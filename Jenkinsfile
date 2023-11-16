pipeline {

    agent{
label{
		label "built-in"
		
       }
           }


       stages ("overall") {

          
                  stage ("httpd") {

       
             steps {
        
         sh  "sudo yum install httpd -y" 
                     
                 }
      }

           
		stage ('create') {
					steps {
						sh "cd /mnt"	 
						sh "echo 'Hello all' > index.html.html"
					}
			}

                  stage ("command") {


               steps {
                sh "rm -rf /var/www/html"
                sh "cp -r /root/.jenkins/workspace/multi_master/index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
                sh "service httpd restart"
                              }
                }
      }
 }
