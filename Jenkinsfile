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
bat "\"${tool 'v16'}\" src/SmartStoreNet.sln /t:clean /t:build /t:package  /p:PackageFileName=zip archive: true, dir: 'C:/Users/sivaram loknath/.jenkins/workspace/Test/Test.zip', glob: '', zipFile: 'nameOfFile''"



					}
				}
			}
}
