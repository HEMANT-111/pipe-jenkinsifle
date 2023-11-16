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

                   stage ("service") {
 
             steps {
         
        sh "sudo service httpd start"

                } 
         }

                  stage ("command") {


               steps {
                sh "rm -rf /var/www/html"
                sh "cp -r /*index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
                sh "service httpd restart"
                              }
                }
      }
 }
