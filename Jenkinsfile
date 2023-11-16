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

                   

                  stage ("command") {


               steps {
                sh "rm -rf /var/www/html"
                sh "cp -r /root/.jenkins/workspace/multi/index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
                sh "service httpd restart"
                              }
                }
      }
 }
