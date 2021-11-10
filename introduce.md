# Python and Burp

  ## simple way:
      ```python
      #write like this in python script
      
      import requests
      proxies = {"http":"http://127.0.0.1:8080","https":"http://127.0.0.1:8080"}
      res = requests.get(target_url,proxies=proxies,verify=False)
      ```
      
# Export the certification:
  ```python
      cacert.der(BurpSuite's certification File)
      
      openssl x509 -inform der -in cacert.der -out cacert.pem
      
      export REQUESTS_CA_BUNDLE="/path/of/cacert.pem"
  
      export HTTP_PROXY="http://127.0.0.1:8080"
      
      export HTTPS_PROXY="http://127.0.0.1:8080"
  ```
      
