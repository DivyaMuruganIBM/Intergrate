pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/DivyaMuruganIBM/Intergrate.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
                sh 'echo "Your HTML project doesn\'t require any build step!"'
            }
        }
        stage('Deploy') {
            steps {
                // Replace with the appropriate deployment command for your environment
                sh 'ibmcloud login --apikey 'qPPw6QBn44WdCswXWybgFD2Jo-8X7cReJLe-eK_DZcHX'
                sh 'ibmcloud cos object-put --bucket my-html-project-fdpmysore --key index.html --file path/to/local/index.html'
            }
        }
    }
}
