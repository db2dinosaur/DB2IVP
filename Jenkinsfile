#!groovy

@Library('SubmitAndTrack') _

def ivpdsn = "not set yet"

pipeline {
  agent { label 'zos' }
  parameters {
    string(name: 'DB2IVP', defaultValue: 'SDB2T.JENKINS.SDSNSAMP', description: 'DB2 for z/OS IVP JCL dataset')
  }
  stages {
    stage('Prepare') {
      steps {
        script {
            ivpdsn = "${params.DB2IVP}";
            println("IVP dataset in use = ${ivpdsn}");
        }
      }
    }
    stage('DSNTEJ0') {
      steps {
        script {
            println("Submitting '${ivpdsn}(DSNTEJ0)'")
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ0)'",8,1200,false))
        }
      }
    }
    stage('DSNTEJ1') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ1)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ1P') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ1P)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ1S') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ1S)'",0,1800,false))
        }
      }
    }
    stage('DSNTEJ1U') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ1U)'",0,1800,false))
        }
      }
    }
    stage('DSNTEJ2A') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2A)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2C') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2C)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2D') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2D)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2E') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2E)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2H') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2H)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2P') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2P)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ2U') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ2U)'",4,1800,false))
        }
      }
    }
    stage('Spufi Tests') {
      steps {
        echo "We should be running DSNTESA, DSNTESC and DSNTESE through Spufi here, but as this is a batch process:"
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ30)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ3C') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ3C)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ3M') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ3M)'",0,1800,false))
        }
      }
    }
    stage('DSNTEJ3P') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ3P)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ6U') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ6U)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ6Z') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ6Z)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ7') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ7)'",4,1800,false))
        }
      }
    }
    stage('DSNTEJ71') {
      steps {
        script {
            println(SubmitAndTrack("'${ivpdsn}(DSNTEJ71)'",4,1800,false))
        }
      }
    }
  }
}
