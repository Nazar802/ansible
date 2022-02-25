node {
    stage ('Scm Chekout') {
        git branch: 'main', url: 'https://github.com/Nazar802/ansible.git'
    }
    
    stage ('Datadog Agent Installation') {
        tool name: 'Ansible', type: 'org.jenkinsci.plugins.ansible.AnsibleInstallation'
        ansiblePlaybook credentialsId: 'private_key', inventory: 'inventory', playbook: 'datadog.yaml'
    }
}
