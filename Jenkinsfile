pipeline{
  agent any
  environment{
     
    branch="${params.branch}"
    host='ubuntu'
    ip="${params.hostIp}"
    jenkinsIp='3.110.116.50'
  }
    stages{
    
      stage('git clone'){
        steps{
         sh '''
         ssh -o StrictHostKeyChecking=no ${host}@${jenkinsIp}'
            cd /home/ubuntu
            mkdir test
         '
         '''
            }
      }
    
    }


}
