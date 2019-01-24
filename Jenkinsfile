@Library('gsl')
def utils = new com.binxhealth.Utils()

buildTemplate(
    timeoutMinutes: 20
) {
    // Run CI on PRs and Master
    if (isBuildRequired()) {
        stage('Publish Release') {
          publish()
        }
        if (isMaster()) {
          promoteTo('ci')
        }
    }
}
