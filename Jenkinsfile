pipeline{
agent any
  stages
  {
    stage('Cloning git')
    {
      steps
            {
      git branch: 'main', url: 'https://github.com/beingKhanvilkar/ansible_project.git'
           }
    }
    stage ('Running ansible file')
    {
      steps {
ansiblePlaybook credentialsId: 'ec2-user', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory.ini', playbook: 'iapache.yml', vaultTmpPath: ''
      }
    }
  
  }
}
}
