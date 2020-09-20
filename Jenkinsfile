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

 bat "\"${tool 'MSBuild'}\" SmartStoreNET.proj /p:SlnName=SmartStoreNET /m /p:DeployOnBuild=true /p:DeployDefaultTarget=WebPublish /p:WebPublishMethod=FileSystem /p:SkipInvalidConfigurations=true /t:build  /p:Platform=\"Any CPU\"  /p:publishUrl=c:\\iis"


					}
				}
			}
}
