pipeline {
    agent any

    stages {


        stage('Build Docker Image') {
            steps {
                // Docker imajını oluştur
                script {
                    sh 'docker image build -t webimage:$version .'
                }
            }
        }


        stage('Deploy') {
            steps {
                // Sunucuda Docker imajını başlat
                script {
                    sh 'docker run webimage:$BUILD_NUMBER' // Veya başka bir komut ile imajı başlatın
                }
            }
        }
    }
}
