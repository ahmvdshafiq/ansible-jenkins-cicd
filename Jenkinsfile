pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/ahmvdshafiq/ansible-jenkins-cicd.git'
      }
    }
    stage('Run Ansible Playbook') {
      steps {
        sh '''
          ansible-playbook -i ansible/inventory/hosts ansible/playbooks/deploy.yml
        '''
      }
    }
  }
}

