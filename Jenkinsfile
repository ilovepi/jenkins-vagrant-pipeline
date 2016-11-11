node{
    stage 'Check Base Box Install'
    // if base box isn't here, install it
    echo 'Verifying Base box installation ...'

    stage 'Build Vagrant Box'
    echo 'Building vagrant VM...'
    vagrant up --provision
    echo 'VM configuration complete'
    echo 'Initiating Build'
    vagrant ssh setup.sh
    vagrant package --name bf.box
    archiveArtifacts artifacts: '*.box', fingerprint: true
}
