pipeline {
        agent {
        label {
        label ('build-in')
        customWorkspace '/data/pipeline'
        }
        }
        stages {
        /*stage ('install-httpd') {
        steps {
        sh "yum install httpd -y"
}
}*/
        stage ('deploy-index') {
        steps {
        sh "cp -r index.html /var/www/html"
        sh "chmod -R 777 /var/www/html/index.html"
}
}
        stage ('Restart httpd') {
        steps {
        sh "service httpd start"
}
}
}
}
