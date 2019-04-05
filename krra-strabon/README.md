## Use Strabon
* `[sudo] docker run --name strabon_container_name -v /<some_local_dir>:/inout -p 9091:8080 gioargyr/krra-strabon:tool` <br />
Now a docker-container is created based on the docker-image gioargyr/krra-strabon:tool. <br />
Feel free to select whatever name you want for the container-name. <br />
Feel free to select whatever port you want for mapping as long as it is available. <br />
In case you want to have files available inside the strabon-docker-container, store them in /<some_local_dir> in your machine. <br />
* `[sudo] docker exec -it strabon_container_name /bin/bash` <br />
In case you want to work inside the container.<br />
It is absolutely necessary to do it and run (while being inside the container) the command `$ runtomcat.sh`

**Attention**  When the container is up and running, it provides only a postgres(+postgis) DBMS. In order to make Strabon available,
you should start container's tomcat as described in the previous instruction.
<br /> <br />
NOW, Strabon is available in you local machine. Open a browser and type `localhost:9091/Strabon`
