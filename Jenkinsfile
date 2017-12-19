#!groovy
node {
    env.SKIP_UNIT_TESTS = 1
    sh "git submodule init"
    sh "git submodule update"
    StandardBuild()
}
