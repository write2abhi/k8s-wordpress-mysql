To test hpa follow below steps:

1. Exec into load-generator pod in wordpress namespace and run below command

while true; do wget -q -O- http://wordpress.wordpress.svc.cluster.local; done