pipeline {
  agent any
     stages {
       stage ("SCM Checkout") {
         steps 
            {
              git branch: 'master', url: 'https://github.com/venkateshg1/app2.git'
            }
                              }
       stage ("Excute Ansible") { 
          steps
              { 
                 ansiblePlaybook credentialsId: 'Ansible', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'apache.yml' 
 
             }
                                }
     }
}
