pipeline{
    agent any
    stages {
        stage('Crear-Directorio') {
            steps{
                ansiblePlaybook credentialsId: 'oracleDB1', installation: 'ansible', inventory: '/etc/ansible/hosts', limit: 'BD', playbook: '/var/lib/jenkins/workspace/prueba-pipeline/createFolder.yml'
            
        }
        stage('Crear-Fichero') {
            steps{
                ansiblePlaybook credentialsId: 'oracleDB1', installation: 'ansible', inventory: '/etc/ansible/hosts', limit: 'BD', playbook: '/var/lib/jenkins/workspace/prueba-pipeline/createFolder.yml'
            }
            
        }
    }
}
