pipeline{
  agent {label "linux"}
  stages{
    stage("build"){
      steps {
        sh """
          docker build -t vopros .
        """  
      
      }
    
    }
    stage("deploy"){
      steps {
        sh """
          docker run -it -p 8000:8000 vopros
        """  
      
      }
    
    }
  }
}
