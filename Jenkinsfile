pipeline {

agent any


       stages ("overall") {

          
                  stage ("httpd") {

       
             steps {
        
         sh  "yum install httpd -y" 
         sh  "service httpd start"            
                 }
      }
                stage ("command") {


               steps {
               
                sh "cp -r /root/.jenkins/workspace/gitpipe_master/index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
	       }
		  }            
           
		stage ("restart") {

			steps {
	   sh "Service httpd restart"
			}

		}
        
      }
 }
