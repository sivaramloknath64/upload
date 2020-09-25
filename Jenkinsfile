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
bat "\"${tool 'v16'}\" src/smartstoreNet.sln /t:clean /t:build /p:Configuration=Release /p:Platform=\"Any Cpu\" "



					}
				}
		
		
		stage('Deploy to iis'){
			steps{
				 echo "Deploying to iis "
		         	
				
					}
				}
			}
}
