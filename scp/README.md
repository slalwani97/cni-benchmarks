1. Build the image
  - cd cni-benchmarks/scp/image
  - docker build -t <username>/scp-test .

2. Replace the image with your image (username/scp-test) in client and server yaml

3. Run the server 
  - kubectl apply -f ssh-server.yaml

4. Run the client
  - kubectl apply -f ssh-client.yaml

5. Now to run the test exec into the client pod 
  - kubectl exec -it <client-pod-name> bash
  - scp sumit@<server-pod-ip>:/home/sumit/200MB.zip ./scp-file.zip
