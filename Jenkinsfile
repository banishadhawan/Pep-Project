pipeline{
    agent any {
        stages
        {
            stage('Checkout') 
            {
                steps {
                    git url:'https://github.com/banishadhawan/Pep-Project.git'
                    branch : 'main'
                }
            }
            stage('Test')
                {
                    steps {
                        sh 'test -f index.html'
                        echo "file found"
                    }
                }
        }
            post{
                success {
                    echo "Pipeline completed successfully."
                }
                failure {
                    echo "Pipeline failed."
                }
            }
    }
}
