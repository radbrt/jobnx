# Neo4j jobs netwprk

## Purpose
This repo is for creating a neo4j container and import a graph of occupations and companies advertising for said occupations. The data is based on an open dataset published by NAV, and subsetted on the part of the data that is annotated with ISCO-08 occupational codes.

The graph is fairly simple, with two node types (occupations and companies), and directed links (as they must be in neo4j) from companies to the occupations they advertise for. Most of the interesting analysis to do on this data does not necssitate a graph database, but, well, it's fun and looks cool.

## Running
Start the docker image by running the docker-compose file. The compose-file will automatically link the folder containing the database to your local filesystem (the /data folder will be populated) and the folder designated for file imports.

The node- and edgefiles are already placed in the import folder, but in order to import them you have to run the commands in the `commands.txt` file through the neo4j command line.

you will find the neo4j browser at localhost:7474, and the default username/password is neo4j/neo4j.
