node('master') {
    // some block
    stage('scm'){
        git 'https://github.com/rvaradharaj1/openmrs-core.git'
        
    }
    stage('build'){
        sh 'mvn clean package'
    }

    stage('postbuild'){
        junit '**/TEST-*.xml'
        archive '**/*.war'

    }
}