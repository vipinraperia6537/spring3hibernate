pipeline{
    agent any
    stages
    {
        
        stage('git')
        {
            steps{
                
                git "https://github.com/opstree/spring3hibernate.git"
            }
        }
        
        stage('CODE STABILITY')
        {
            steps{
                sh "mvn compile"
            }
            
        }
        
        stage('CODE QUALITY'){
            steps{
                
                sh "mvn checkstyle:checkstyle"
            }
        }
        stage('CODE COVERAGING'){
            steps{
                

                
                sh "mvn cobertura:cobertura"
            }
        }
    }
}
