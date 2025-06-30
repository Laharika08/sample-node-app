pipeline{
    agent any
   
    stages{
        stage('checkout'){
           steps{
             git url: 'https://github.com/Laharika08/sample-node-app.git' , branch: 'master'
           }
        }
        stage('Install dependencies'){
           steps{
              bat 'npm install'
           }
         }
         stage('Test'){
            steps{
               bat 'npm test'
            }
         }
         stage('Deploy'){
            steps{
                echo "deploy after test pass"
            }
         }
     }
    post{
      success{
         echo "success when test pass"
      }
      failure{
         echo "failed when test fail"
      }
     }
}

