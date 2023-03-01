pipeline {
  agent any
     stages {
       stage ("SCM Checkout") {
         steps 
            {
              sh 'git credentialsId: 'Git', url: 'https://github.com/venkateshg1/app2.git' '
                                                  }
       }
       stage ("Excute Ansible") { 
          steps
              { 
                 sh 'ansiblePlaybook credentialsId: 'Ansible', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'apache.yml' '
 
              }
           }
     }
}
