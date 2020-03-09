## Use GeoTriples
* `[sudo] docker run --name geotriples-container-name -v /<some_local_dir>:/inout gioargyr/krra-geotriples:tool` <br />
Now a docker-container is created based on the docker-image gioargyr/krra-geotriples:tool.
Feel free to select whatever name you want for the container-name.<br />
* `[sudo] docker exec -it geotriples-container-name /bin/bash <br />`
Now you are inside the container's CLI and you can use geotriples.

## GeoTriples Usage
* Go to the /bin directory of GeoTriples: `cd /<path_to_geotriples-1.1.6-bin>/bin`
* Run geotriples-all in order to see all available options and examples: `./geotriples-all`
