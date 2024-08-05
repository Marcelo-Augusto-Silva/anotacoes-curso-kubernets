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




