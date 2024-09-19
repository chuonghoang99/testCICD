pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Lấy mã nguồn từ Git repository
                git url: 'https://github.com/chuonghoang99/testCICD.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Build ứng dụng, ví dụ với Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Chạy các bài kiểm thử tự động
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Triển khai ứng dụng lên môi trường staging
                sh './deploy.sh'
            }
        }
    }

    post {
        // Gửi thông báo nếu pipeline thành công
        success {
            echo 'Pipeline đã thành công!'
        }

        // Gửi thông báo nếu pipeline thất bại
        failure {
            echo 'Pipeline đã thất bại.'
        }
    }
}
