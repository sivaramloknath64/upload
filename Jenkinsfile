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
bat label: '', script: '''
					 "\"${tool \'MSBuild\'}\" SmartStoreNET.proj /p:SlnName=SmartStoreNET /t:clean; t/:build t:/package /p:Platform=\"Any CPU\"/p:PackageFileName="C:\Users\sivaramloknath\.jenkins\workspace\TestJenkins\TestJenkins.zip  /p:Configuration=Release "

'''
}

					}


		stage('deploy'){
			steps{
				 echo "deploy"
		         	bat label: '', script: ''' \'C:\"Program Files (x86)"\IIS\"Microsoft Web Deploy V3"\msdeploy.exe -verb:sync -source:package="TestJenkins"
dest:contentPath="www.again.com",computerName=localhost -allowUntrusted=true\'

'''				
					}
				}




				}
			}

