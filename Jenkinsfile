pipeline{
    agent any
    stages {
        stage('Crear-Directorio') {
            steps{
                ansiblePlaybook credentialsId: 'oracleDB', installation: 'ansible', inventory: '/etc/ansible/hosts', limit: 'BD', playbook: '/var/lib/jenkins/workspace/prueba-pipeline-file/createFolder.yml'
            }    
            
        }
        stage('Crear-Fichero') {
            steps{
                ansiblePlaybook credentialsId: 'oracleDB', installation: 'ansible', inventory: '/etc/ansible/hosts', limit: 'BD', playbook: '/var/lib/jenkins/workspace/prueba-pipeline-file/createArchive.yml'
            }
            
        }
    }
}
