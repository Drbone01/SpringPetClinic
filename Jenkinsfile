pipeline[
    agent{label 'master'}
    tools{maven 'M3'}
    stages(
        stage('Checkout'){
            steps{
                git branch: 'main' , url; 'https://github.com/Drbone01/SpringPetClinic.git'
            }
        }
        Stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        Stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
            sh 'mvn package'
        }
        stage('Deploy'){
            steps{
                sh 'java-jar /var/lib/jenkins/workspace/PetClinicDecPipeline/target/*.jar'
            }
        }
    
    ]
