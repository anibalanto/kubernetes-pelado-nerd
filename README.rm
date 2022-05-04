# kubernetes
##  [video Kubernetes-Terraform Lamansys (Silvana)](https://drive.google.com/file/d/10tZjuXoNPaGOhmeGVHIYiYmKLYpKESE6/view)
##  [video pelado nerd](https://www.youtube.com/watch?v=DCoBcpOA7W4)
##  [libro](https://sre.google/sre-book/table-of-contents/)
##  [documentación](https://kubernetes.io/docs/home/)
##  orquestador
##  Instancias
###   en Docker: cuidar
####    nombrada
####    como mascota
###   en Kubernetes: descartables
####    no te importa que muera
####    como ganado :(
##  declarativo: manifiesto
##  Componentes
###   [image](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/components-of-kubernetes.svg)
###   * control plane
####    los servidores de kubernetes
####    se encargan de operaciones de orquestación
###   ** node
####    o instancias
####    recursos que van a correr contenedores
###   API server *
####    trabaja con contenedores
####    los distribuye en Workers
####    si se cae un Worker
#####     intenta recuperarse automáticamente
#####     si no contamos con más instancias no va a poder
###   Cloud controller manager *
####    Se conecta a al API del proveedor de cloud
#####     crear load balancer
#####     crear/destruir instancias
#####     pedir disco virtual y conectar a instancia
####    lo diferenecia de docker compose
####    conectar con 
#####     amazon
#####     google
#####     digital-ocean
###   Controller Manager *
###   etcd *
####    persistence sotre
####    basada en key value
####    estado del cluster
###   Scheduler *
####     Mueve los contenedores de un worker a otro
###   kubelet **
####    conectar todos los workers entre sí
####    agenete de kubernetes
###   kube-proxy **
####    recibir el trafico y mandarlo donde tiene que ir
##  para pruebas
###   kubectl
####    para crear y conectar a cluster (lo usamos localmente)
####    [link instalación](https://docs.aws.amazon.com/es_es/eks/latest/userguide/install-kubectl.html)
####    versión: `$ kubectl version --client=true`
####    correr kubernetes
#####     win/mac:  doker-dekstop -> preferences
#####     linux:    [minicube](https://minikube.sigs.k8s.io/docs/)
####    comandos
Basic Commands (Beginner):
  create        Create a resource from a file or from stdin
  expose        Take a replication controller, service, deployment or pod and
expose it as a new Kubernetes service
  run           Run a particular image on the cluster
  set           Set specific features on objects

Basic Commands (Intermediate):
  explain       Get documentation for a resource
#####     recursos
######      get
- Display one or many resources
- obtener recursos
- nodes -> muestra nodos

######      edit
- Edit a resource on the server
- editar un recurso
 
######      delete
- Delete resources by file names, stdin, resources and names, or
- borrar un recurso

by resources and label selector

Deploy Commands:
  rollout       Manage the rollout of a resource
  scale         Set a new size for a deployment, replica set, or replication
controller
  autoscale     Auto-scale a deployment, replica set, stateful set, or
replication controller

Cluster Management Commands:
  certificate   Modify certificate resources.
  cluster-info  Display cluster information
  top           Display resource (CPU/memory) usage
#####     manejar nodos    
######      cordon
- Mark node as unschedulable
- ese nodo no recibe mas contenedores
######      uncordon
- Mark node as schedulable
- recibe contenedores
######      drain
- Drain node in preparation for maintenance
- sacar los contenedores para mover a otro lado
  
  taint         Update the taints on one or more nodes

Troubleshooting and Debugging Commands:
  describe      Show details of a specific resource or group of resources
#####     manejar contenedores
######      logs
- Print the logs for a container in a pod
  attach        Attach to a running container
######      exec
- Execute a command in a container
- muy parecido a docker exec
######      port-forward
- Forward one or more local ports to a pod
- si el contenedor expone un puerto puedo accederlo desde mi pc

  proxy         Run a proxy to the Kubernetes API server
######      cp
- Copy files and directories to and from containers

  auth          Inspect authorization
  debug         Create debugging sessions for troubleshooting workloads and
nodes

Advanced Commands:
  diff          Diff the live version against a would-be applied version
#####     apply
######      Apply a configuration to a resource by file name or stdin
######      aplicar un manifiesto a un cluster de kubernetes
  patch         Update fields of a resource
  replace       Replace a resource by file name or stdin
  wait          Experimental: Wait for a specific condition on one or many
resources
  kustomize     Build a kustomization target from a directory or URL.

Settings Commands:
  label         Update the labels on a resource
  annotate      Update the annotations on a resource
  completion    Output shell completion code for the specified shell (bash, zsh
or fish)

Other Commands:
  alpha         Commands for features in alpha
  api-resources Print the supported API resources on the server
  api-versions  Print the supported API versions on the server, in the form of
"group/version"
#####     config
######      Modify kubeconfig files
######      `kubectl config get-context`
- muestra los contextos que están en tu archivo .kubeconfig


  plugin        Provides utilities for interacting with plugins
  version       Print the client and server version information

Usage:
  kubectl [flags] [options]
