pipeline {
	agent any
	stages {
		stage('nugget restore'){
			steps{
				 echo "nugget restoring packages"
		         	bat 'C:/tools/nuget.exe  restore  src/SmartStoreNet.sln'
				
					}
				}

				stage('Build') {
    					steps {
                                        echo " building "
						 bat "\"${tool 'v16'}\"  SmartStoreNET.proj /p:SlnName=SmartStoreNet /t:build /p:Configuration=Release /p:Platform=\"Any CPU\" "
    					}
				}

				stage('build files') {
    					steps {
                                        echo " buildingg "
						 bat "\"${tool 'v16'}\" SmartStoreNET.proj /p:SlnName=SmartStoreNET /m /p:DebugSymbols=false /p:DebugType=None /maxcpucount "
    					}
				}
		
		
		stage(" zipping folder"){
          steps{
             script{
                    zip archive: true, dir: 'C:/Users/sivaram loknath/.jenkins/workspace/Test/build/Web', glob: '', zipFile: 'build.zip'
             }
          }
		}
	
	
	
	
	}

}
