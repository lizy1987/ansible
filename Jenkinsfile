pipeline{
    agent any
    stages {
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
