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
				bat "Deploying to iis ""C:\Program Files\IIS\Microsoft Web Deploy V3\msdeploy.exe" `
  -verb:sync `
  -source:package=`"$package`" `
  `-dest=auto,ComputerName=`"$compname`" `
  `-setParam=name=`"$appname`",value=`"$appValue`" `
  -allowUntrusted
					}
				}
			}
}
