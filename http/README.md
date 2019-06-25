1. build the image.
  - cd cni-benchmarks/http/nginx-image/
  - docker build -t <username>/nginx-test .
  - docker push <username>/nginx-test
  
2. Running the nginx server.
  - kubectl create deployment nginx --image=<username>/nginx-test
  - kubectl create service nodeport nginx --tcp=80:80 or kubectl create service clusterip nginx --tcp=80:80
  
3. Replace the pod ip with your nginx server pod ip in the client yaml.

4. Replace the hostname with your configured hostname in which you have to run the client (It should be different from node of nginx server).

5  kubectl apply -f http-client-pod.yaml

6. To get the results.
  - kubectl logs -f <client-pod>
