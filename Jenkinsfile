pipeline {

    agent {
        label 'local'
    }

	tools {
		jdk 'jdk-11.0.4'
	}

	parameters {
		string name: 'TAG_APP', defaultValue: '', description: 'Tag para imagen docker correspondiente', hidden: true
		booleanParam name: 'BUILD', defaultValue: true, description: 'Activa la construcción de artefactos'
	}

	stages {
		stage('Auditoria Ejecucion') {
			steps{
				echo '------------> Auditoria Ejecucion <------------'
			}
		}

        stage('Preparación de Ambiente') {
			steps{
				echo '------------> Preparación de Ambiente <------------'
			}
		}
		stage('Construccion Artefactos'){
			stages {
				stage('Checkout') {
					steps {
						echo '------------> Checkout <------------'
					}
				}

				stage('Build') {
					steps {
						echo '------------> Build <------------'
					}
				}

				stage('Unit Tests') {
					steps {
                        echo '------------> Unit Tests <------------'
					}
				}

				stage('Publicar Imagenes Docker') {
				    steps {
					    echo '------------> Publicar Imagenes Docker <------------'
					}
				}

			}
		}
	}
}
