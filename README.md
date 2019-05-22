# pub_cert

### 加密

````
docker run --rm -it -v ${PWD}:/src v7lin/openssl:1.1.1b sh -c "openssl enc -e -${ENC_METHOD} -k ${ENC_PASSWORD} -in /src/credentials.json -out /src/credentials.json.enc"
````

### 解密

````
docker run --rm -it -v ${PWD}:/src v7lin/openssl:1.1.1b sh -c "openssl enc -d -${ENC_METHOD} -k ${ENC_PASSWORD} -in /src/credentials.json.enc -out /src/credentials.json"
````
