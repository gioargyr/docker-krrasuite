## Use Sextant tool
* `[sudo] docker run --name sextant_container_name -v /<some_local_dir>:/inout -p 9090:8080 gioargyr/krra-sextant:tool` <br />
Now a docker-container is created based on the docker-image gioargyr/krra-sextant:tool. <br />
Feel free to select whatever name you want for the container-name. <br />
Feel free to select whatever port you want for mapping. As long as it is available. <br />
In case you want to have files available inside the sextant-docker-container, store them in /<some_local_dir> in your machine. <br />
Sextant is available in you local machine. Open a browser and type `localhost:9090/Sextant_v2.0`
* `[sudo] docker exec -it sextant-container-name /bin/bash <br />`
In case you want to be inside the container and change configuration or do anything else.

## Sextant Configuration
Sextant is one of the tools that come with the KRRA-suite. To change the default configurations you can alter the server-configuration.properties file
that is located under /Sextant/WEB-INF/classes/server/
There you can change the default SPARQL endpoint that is used to store and load maps, set PROXY server configuration
and use your Bing Maps key to get access to the Bing Maps base tiles.
For more detailed information you can view the embedded Manual Pages by pressing the "?" button in the top-right corner of the interface.
