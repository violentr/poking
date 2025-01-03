### Usefull information

### Access the Tomcat manager

By default Tomcat manager available from localhost only!

In order to access Tomcat manager remotely settings needs to be changed

`/usr/local/tomcat/webapps/manager/META-INF/context.xml`

#### Build image
```bash
$ docker build -t tomcat_web . 
```
#### Run image
```bash
$ docker run -it tomcat_web -p 80:8080
```
#### Open browser

`http://localhost/manager/html`

Creds: tomcat/s3cret

### Extract war file 

```bash
$ java -xvf sample.war
```
