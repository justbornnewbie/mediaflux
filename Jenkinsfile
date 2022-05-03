pipeline {
  agent
    {
        label 'mf-test-vm'
    }
    stages {
        stage('Download-files-from-azure') {
            steps {
                sh '''
                wget -O azcopy_v10.tar.gz https://aka.ms/downloadazcopy-v10-linux && tar -xf azcopy_v10.tar.gz --strip-components=1
                azcopy copy 'https://dfciiamediaflux.blob.core.windows.net/proactive/*' '/opt/downloads/'  --include-after '2020-08-19T15:04:00Z'
                '''
            }
        }
    
    }
}
