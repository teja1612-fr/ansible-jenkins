pipeline {
    agent any

    environment {
        INVENTORY = 'inventory.ini'
        PLAYBOOK = 'playbook.yml'
    }

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
                    inventory: "${INVENTORY}",
                    playbook: "${PLAYBOOK}",
                    disableHostKeyChecking: true
                )
            }
        }
    }
}
