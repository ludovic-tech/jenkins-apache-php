node{
    stage('Clone git') {
        checkout scm
    }
    stage('Prerequis'){

    	sh apk add ansible sshpass
	sh rm -rf /root/.ssh
	sh ssh-keygen -q -t rsa -N '' -f ~/.ssh/id_rsa
	sh sshpass -p 'root' ssh-copy-id -o stricthostkeychecking=no root@10.0.0.210
    }
    stage('Ansible') {
      ansiblePlaybook (
          colorized: true,          
          playbook: 'playbook.yaml',
          inventory: 'hosts.yaml'
      )
    }
}
