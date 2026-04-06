pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/teja1612-fr/ansible-jenkins.git'
            }
        }

        stage('Run Ansible') {
            steps {
                ansiblePlaybook(
                    credentialsId: 'ansible-key',
                    inventory: 'inventory.ini',
                    playbook: 'playbook.yml',
                    disableHostKeyChecking: true
                )
            }
        }
    }
}
