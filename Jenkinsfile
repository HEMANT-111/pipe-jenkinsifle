pipeline {

agent any


       stages ("overall") {

          
                  stage ("httpd") {

       
             steps {
        
         sh  "sudo yum install httpd -y" 
                     
                 }
      }
                stage ("command") {


               steps {
               
                sh "*/**/index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
	       }
		  }            
           
		stage ("restart") {

			steps {
	   sh "sudo Systemctl restart httpd"
			}

		}
        
      }
 }
