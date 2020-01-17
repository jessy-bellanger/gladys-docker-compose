# gladys-docker-compose

This is how to create an development environment for Gladys v3 or Gladys v4:

## Gladys v3 development environment
**TODO**

## Gladys v4 development environment
Firstly, create an **empty** directory in this folder like so: `gladys-4/sources`. The `sources` folder will contain the Gladys v4 sources when the `gladys-4` service will be started for the first time. Once the needed folders are created, you can run the command `docker-compose up gladys-4` to run Gladys v4 on your machine.

*Important: the `sources` folder **must** be absolutely **empty**, otherwise you will get the following error: `npm ERR! missing script: start:prod`, meaning that the sources have not been loaded. If you get it, delete the `sources` folder and re-create it.*

The Gladys v4 web interface will be reachable at http://localhost and its sources will be loaded into the `gladys-4/sources` directory. From here you can do whatever you want with the sources. To apply your changes, run the command `docker-compose restart gladys-4`. A `db` folder is automatically created when Gladys v4 is started. It contains the database used by Gladys.