This repo consists of k8s mnifest files to deploy a two tier Wordpress MySQL application. 

Wordpress is deployed to *wordpress* namespace and MySQL is deployed to *mysql* namespace. 

- To test hpa follow below steps:

    kubectl run -i --tty load-generator --image=busybox /bin/sh

    Hit enter for command prompt

    while true; do wget -q -O- http://wordpress.wordpress.svc.cluster.local; done


Note: 
A load-generator pod is alredy crated in wordpress namespace. 

To access wordpress in browser use below command to get external IP:
kubectl get svc wordpress -n wordpress

To access the currently running wordpress application use below url:
http://35.226.8.31
