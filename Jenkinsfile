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
bat "\"${tool 'v16'}\" src/smartstoreNet.sln /t:clean /t:build  "



					}
				}
		
		
		stage('build'){
			steps{
				 echo "nugget restoring packages"
		         	bat 'ClickToBuild'
				
					}
				}
			}
}
