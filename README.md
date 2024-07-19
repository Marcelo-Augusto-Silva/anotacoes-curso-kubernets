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