node {
    stage ('Scm Chekout') {
        git branch: 'main', url: 'https://github.com/Nazar802/ansible.git'
    }
    
    stage ('Datadog Agent Installation') {
        ansiblePlaybook credentialsId: 'private_key', installation: 'Ansible', inventory: 'inventory', playbook: 'datadog.yaml'
    }
}
