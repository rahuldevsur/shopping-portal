pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('Build'){
            steps{
                echo 'this is the Build job'
                sh 'npm install'
            }
        }
        stage('Test'){
            steps{
                echo 'this is the Test job'
                sh 'npm test'
            }
        }
        stage('Package'){
            steps{
                echo 'this is the third job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
