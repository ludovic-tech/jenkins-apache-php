node{
    stage('Clone git') {
        checkout scm
    }
    stage('Ansible') {
      ansiblePlaybook (
          colorized: true,          
          playbook: 'playbook.yaml',
          inventory: 'hosts.yaml'
      )
    }
}
