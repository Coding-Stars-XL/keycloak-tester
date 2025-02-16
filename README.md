# Welcome to my Keycloak stack for local development and testing!

Please Read the instructions below to deploy the stack with docker-compose!

***NOTE: You will need docker/docker-desktop installed on your system before you attempt this***
_________________________________________________________________________________________________

**Create working directory, clone the repo, and build your images**

- ***Windows(PowerShell)/Linux/Mac***
  -  Change to the directory where you would like to clone the repo
  -  git clone https://github.com/coreypell/test-identity.git .
  -  cd test-identity

__________________________________________________________________________________________________

**Create a ".env" file in the main directory where the docker-compose.yml is**

- ***Populate the ".env" file with the following variables***
  - DB_NAME=changeme
  - DB_USER=changeme
  - DB_PASS=changeme
  - KC_ADMIN_USER=changeme
  - KC_ADMIN_PASS=changeme

*Special note for FIPS Deployments: All passwords need ot be at least 16 characters*
*Note: make sure you populate variables with your own information (delete the "changeme" and use your own)*
*Note: I would suggest changing the "DB_USER" to "postgres" to avoid issues*

__________________________________________________________________________________________________

**Deploy your stack!**

While you are in the "test-identity" directory run:

  -  docker-compose up -d

The Docker Compose will build the images for you if this is your first time.
This will take some time, so please allow the process to complete!

From here you can navigate to https://localhost/auth to get to Keycloak.

_________________________________________________________________________________________________

Clean up!
  -  docker-compose down -v

The "-v" option deletes named volumes for a full cleanup!
If you wish to retain the named volumes, simply remove the "-v" option.

**Enjoy!**
