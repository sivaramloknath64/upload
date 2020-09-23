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
bat "\"${tool 'v16'}\" /p:src/SmartStoreNet.sln /t:clean;build;package  /p:PackageFileName='C:/Users/sivaram loknath/.jenkins/workspace/Test'"



					}
				}
			}
}
