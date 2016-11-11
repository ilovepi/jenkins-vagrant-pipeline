node{
    stage 'Build Vagrant Box'
    vagrant up --provision
    vagrant ssh setup.sh
    vagrant package
}
