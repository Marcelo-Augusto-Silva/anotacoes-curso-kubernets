Anotações do Curso de Kubernets


kubectl run nginx-pod --image=nginx:latest = Esse comando cria um pod nginx com a ultima versão 

kubectl get pods =  mostra todos os pods criados

kubectl apply -f [nome do arquivo] = subir um pod com um arquivo que voce criou 

kubectl edit pod nginx-pod = comando para editar o pod 

kubectl describe pod = descreve o pod 

kubectl delete pod [nome do pod] = Deletar um pod

kubectl delete -f primeiro-pod.yaml = deletar um pod passando arquivo