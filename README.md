Anotações do Curso de Kubernets


kubectl run nginx-pod --image=nginx:latest = Esse comando cria um pod nginx com a ultima versão 

kubectl get pods =  mostra todos os pods criados

kubectl apply -f [nome do arquivo] = subir um pod com um arquivo que voce criou 

kubectl edit pod nginx-pod = comando para editar o pod 

kubectl describe pod = descreve o pod 

kubectl delete pod [nome do pod] = Deletar um pod

kubectl delete -f primeiro-pod.yaml = deletar um pod passando arquivo

kubectl get pod -o wide = mostra todos os pods e os ips de cada pod

kubectl get svc [ou service] = comando usado para listar os services

kubectl exec -it [nome do pod] -- bash = comando para abrir o bash no pod 

Cluster Ip é um servico que faz com que outros pods se comuniquem 


Node Port seve para abrir comunicação para o mundo externo, permitir que o host ou outros computadores acessem o pod

kubectl get nodes -o wide = mostra todos os nodesport e com descricao

No nodes, windows ele usa o ip localhost
No linux usa o ip do Node

kubectl delete pods --all = Apaga todos os pods

kubectl delete svc --all = Apaga todos os serviços

mysql -u root -p = comando para entrar com o usuario root no pod de banco de dados

configmap serve para colocarmos a confiuraçao de arquivos

kubectl get configmap = mostra todos os configmap




Anotações da parte 2 do curso da alura



Replica Set serve para encapsular um ou mais pods e pode gerenciar um ou mais pod

kubectl get rs = mostra todos os replicaset
kubectl get replicaset = mostra todos os replicaset

Deployment e replicasets servem para a mesma função

O deployment ele tem uma camada a mais que o replicaset, quando você cria um deployment, automaticamente você está criando um replicaset

Assim como para versionar o codigo temos o Git, para versionar a versao do container temos o Deployment

kubectl rollout history deployment nginx-deployment = mostra todas as alterações que teve no Deployment

kubectl apply -f nginx-deployment.yaml --record = atualiza o pod e deixa registrado 

kubectl annotate deployment nginx-deployment kubernetes.io/change-cause="Definindo  a imagem com versão latest" = Esse comando server para você deixar escrito o que você alterou no deployment, nesse caso colocamos "Definindo a imagem com versão latest"

kubectl rollout undo deployment nginx-deployment --to-revision=1  = Esse comando server para você voltar uma versâo que você quer 


Persistencia de dados

Os volumes servem para manter a persistencia dos dados, os Volumes possuem ciclos de vida independentes dos containers porém são dependentes dos pods

Para criar um volume no linux voce tem que criar a pasta quee irá ser compartilhada dentro do minikube, voce rodaa o seguinte comando

minikube ssh = irá entrar dentro do minikube, após isso você deverá criar a pasta que seŕa compartilhada

Você tbm pode colocar o Type = DirectoryOrCreate e ele irá criar o volume se não tiver a pasta especificadaa 

Um StatefulSet serve para manter a persistencia dos dados, quando um pod é riniciado ele não perde os dados

