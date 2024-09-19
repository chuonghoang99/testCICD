pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Lấy mã nguồn từ Git repository
                git 'https://github.com/chuonghoang99/testCICD.git'
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
