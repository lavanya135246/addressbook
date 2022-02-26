pipeline {
   agent 
    { 
        node 
        { 
            label 'master' 
        } 
    } 

    tools
    {
        maven 'Apache Maven 3.6.3'
        jdk 'JDK'
    }

    stages
    {
        stage('Validate code')
        {
            steps{
                sh ' mvn validate'
            }
        }
        stage('Code Compile') {
                steps {
                    sh 'mvn compile'
                }
            }
        stage('Code Test') {
                steps {
                sh 'mvn test'
                }
            }
        stage('Package') {
                steps {
                sh 'mvn package'
                }
            }
 
    }
}