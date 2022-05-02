pipeline {
    agent any
    stages {
        stage('Download-files-from-azure') {
            steps {
                sh '''
                azcopy copy 'https://dfciiamediaflux.blob.core.windows.net/proactive/*' '/opt/downloads/'  --include-after '2020-08-19T15:04:00Z'
                '''
            }
        }
    
    }
}
