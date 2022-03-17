node{
    stage('Clone git') {
        checkout scm
    }
    stage('Lancement du Ansible') {
      ansiblePlaybook (
          colorized: true,          
          playbook: 'playbook.yaml',
          inventory: 'hosts.yaml'
      )
    }
}
