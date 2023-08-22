pipeline{
    agent any
    stages {
        stage('Clonar-Repo') {
            steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/lizy1987/ansible.git']]])
            }
            
        }
		stage('Crear-Directorio') {
            steps{
                ansiblePlaybook credentialsId: 'ubuJenkis', disableHostKeyChecking: false, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/var/lib/jenkins/workspace/prueba-pipeline/createFolder.yml'
            }
            
        }
        stage('Crear-Fichero') {
            steps{
                ansiblePlaybook credentialsId: 'ubuJenkis', disableHostKeyChecking: false, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/var/lib/jenkins/workspace/prueba-pipeline/createArchive.yml'
            }
            
        }
    }
}
