pipeline {

    agent{
label{
		label "slave-3"
		customWorkspace "/mnt/remoteslave3"
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
                sh "cp -r /mnt/remoteslave3/index.html /var/www/html"
                sh "chmod -R 777 /var/www/html"
                sh "service httpd restart"
                              }
                }
      }
 }
