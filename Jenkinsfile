node {
  
  stage TEST
  sh 'echo ok'

  stage 'Build'
  checkout scm
  sh '''
    lein test
    lein jar
  '''

  stage 'Publish'
  slsSetPackageVars('clojure', 'project.clj')
  sh '''
    # not implemented yet
    echo "jfrog rt u $PACKAGE_NAME/target/$PACKAGE_NAME-$PACKAGE_VERSION.jar yieldbot-clojure/$PACKAGE_NAME/$PACKAGE_VERSION/ --url=https://artifactory.yb0t.cc/artifactory --dry-run"
  '''

  stage 'Deploy'
  sh '''
    # not implemented yet
  '''

}
