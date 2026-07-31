pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    installation: 'ansible-local',
                    playbook: 'deploy.yml',
                    inventory: 'inventory',
                    colorized: true
                )
            }
        }
    }
}
