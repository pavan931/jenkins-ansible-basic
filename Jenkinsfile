pipeline{
    agent any
    environment {
        ANSIBLE_HOST_KEY_CHECKING = "False"
    }
    stages{
        stage('checkout'){
            steps{
                git url:"https://github.com/pavan931/jenkins-ansible-basic.git" , branch:'main',
                credentialsId:'git-creds'
            }
        }
        stage('Running a playbook'){
            steps{
                sh 'ansible-playbook -i hosts.ini nginx.yml'
            }
        }
    }
}
