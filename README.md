**Crie uma imagem:**

```
docker build -t jenkins/jenkins:v1.0 .
```

**Em seguida, execute a imagem atualizada do Jenkins enquanto passa as variáveis ​​de ambiente JENKINS_ADMIN_ID e por JENKINS_ADMIN_PASSWORD (substitua <password> por uma senha de sua escolha):**

```
docker run -d  -v jenkins_vol:/var/jenkins_home -p 8080:8080 -p 50000:50000 --env JENKINS_ADMIN_ID=admin --env JENKINS_ADMIN_PASSWORD=password --name jenkins_r2d2 jenkins/jenkins:v1.0
```

**Se caso quiser usar o docker-compose: passe os valores no environment em docker-compose.yaml**

```
docker-compose up -d
```
**Caso queira atualizas os plugins é só editar o arquivo ```plugins.txt``` com as novas versões e depois buildar uma nova imagem**
