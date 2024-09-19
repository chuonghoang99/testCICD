pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/chuonghoang99/testCICD.git',
                        refspec: '+refs/heads/*:refs/remotes/origin/*'
                    ]]
                ])
        }

    }

    // post {
    //     // Gửi thông báo nếu pipeline thành công
    //     success {
    //         echo 'Pipeline đã thành công!'
    //     }

    //     // Gửi thông báo nếu pipeline thất bại
    //     failure {
    //         echo 'Pipeline đã thất bại.'
    //     }
    // }
}
