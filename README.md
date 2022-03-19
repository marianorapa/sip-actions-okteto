# K8S on Okteto with GitHub Actions

Clonando este repo y siguiendo estos pasos, tendremos un CI/CD funcionando con Github Actions y Okteto:

0. Crear cuenta en okteto y repo en github
1. Configurar secrets en Github > Settings > Actions > Repository Secret:
	1. Encodear en base64 el kubeconfig de okteto (descarga de la web) y poner el valor en el secret KUBE_CONFIG_DATA
    2. Secrets DOCKER_USERNAME y DOCKER_PASSWORD con el nombre de usuario de Dockerhub y password, respectivamente.
2. Cambiar el nombre de la imagen/repo en  deployment/deployment.yaml y en workflows/cicd.yaml
3. Aplicar deployment a mano la primera vez. Para eso, configurar acceso al cluster de k8s como indica Okteto: desde la web, Settings > Download Config File. Nos descarga el archivo de configuración, y ejecutamos el comando para agregar el contexto.
