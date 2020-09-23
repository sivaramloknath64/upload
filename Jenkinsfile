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

 bat "\"${tool 'MSBuild'}\" SmartStoreNET.proj /p:SlnName=SmartStoreNET /t:clean;build;package /p:PackageFileName='C:\Users\sivaram loknath\.jenkins\workspace\Test\Test.zip'"


					}
				}
			}
}
