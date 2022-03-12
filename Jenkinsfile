
  def buildEnvironment = "${SDLC}"
    node{
     
        stage('Read Parameters') {
              echo 'Hello World' 
              echo "FirmPlusEnterprise_Branch Name - ${env.FirmPlusEnterprise_Branch}"
              echo "API_Branch Name - ${env.API_Branch}"
            
        dir('FirmPlusEnterprise') 	{
			git branch: '${env.FirmPlusEnterprise_Branch}', url: 'https://${TOKEN}@dev.azure.com/fi360/_git/Fi360-Platform-Mercury'
		}
        dir('API') 	{
			git branch: '${env.API_Branch}', url: 'https://${TOKEN}@dev.azure.com/fi360/_git/DPP-Data-Processing-Platform'
		}
       }
        
        stage('Scan'){
        
                    
step([$class: 'CxScanBuilder', addGlobalCommenToBuildCommet: true, avoidDuplicateProjectScans: true, comment: '', configAsCode: true, credentialsId: 'Ravi Bethala CheckMarx Login', customFields: '', excludeFolders: '', exclusionsSetting: 'global', failBuildOnNewResults: false, failBuildOnNewSeverity: 'HIGH', filterPattern: '''!**/_cvs/**/*, !**/.svn/**/*,   !**/.hg/**/*,   !**/.git/**/*,  !**/.bzr/**/*, !**/bin/**/*,
!**/obj/**/*,  !**/backup/**/*, !**/.idea/**/*, !**/*.DS_Store, !**/*.ipr,     !**/*.iws,
!**/*.bak,     !**/*.tmp,       !**/*.aac,      !**/*.aif,      !**/*.iff,     !**/*.m3u, !**/*.mid, !**/*.mp3,
!**/*.mpa,     !**/*.ra,        !**/*.wav,      !**/*.wma,      !**/*.3g2,     !**/*.3gp, !**/*.asf, !**/*.asx,
!**/*.avi,     !**/*.flv,       !**/*.mov,      !**/*.mp4,      !**/*.mpg,     !**/*.rm,  !**/*.swf, !**/*.vob,
!**/*.wmv,     !**/*.bmp,       !**/*.gif,      !**/*.jpg,      !**/*.png,     !**/*.psd, !**/*.tif, !**/*.swf,
!**/*.jar,     !**/*.zip,       !**/*.rar,      !**/*.exe,      !**/*.dll,     !**/*.pdb, !**/*.7z,  !**/*.gz,
!**/*.tar.gz,  !**/*.tar,       !**/*.gz,       !**/*.ahtm,     !**/*.ahtml,   !**/*.fhtml, !**/*.hdm,
!**/*.hdml,    !**/*.hsql,      !**/*.ht,       !**/*.hta,      !**/*.htc,     !**/*.htd, !**/*.war, !**/*.ear,
!**/*.htmls,   !**/*.ihtml,     !**/*.mht,      !**/*.mhtm,     !**/*.mhtml,   !**/*.ssi, !**/*.stm,
!**/*.stml,    !**/*.ttml,      !**/*.txn,      !**/*.xhtm,     !**/*.xhtml,   !**/*.class, !**/*.iml, !Checkmarx/Reports/*.*''', fullScanCycle: 10, groupId: '28', password: '{AQAAABAAAAAQ0oVAlOSkWiyzscesrzfVui5RBK3EoTyRSHloq5ii5sA=}', postScanActionId: 1, preset: '100001', projectName: 'FIRMPLUS ENTERPRISE(2105)_DEV', sastEnabled: true, serverUrl: 'https://checkmarx.broadridge.net', sourceEncoding: '1', useOwnServerCredentials: true, username: '', vulnerabilityThresholdResult: 'FAILURE', waitForResultsEnabled: true])
}
        
        }   


        
 }

