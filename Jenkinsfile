pipeline {

agent any


       stages ("overall") {

          
                  stage ("httpd") {

       
             steps {
        
         sh  "yum install httpd -y" 
                     
                 }
      }

	       
             steps ("service"){
        
         sh  "sudo systemctl start httpd"

                     
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
	   sh "sudo systemctl restart httpd"
			}

		}
        
      }
 }
