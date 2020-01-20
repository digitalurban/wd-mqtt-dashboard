# MQTT Weather Dashboard 

Dashboard to display environmental data from Weather Display MQTT Output - the code is editable for other MQTT feeds.

## Configuration




### Setting up Passwords
Copy and rename the file `.env.template` to `.env` and enter a value for the root mysql user as well as the MySQL username and password. These values will persit into the node application 
so you don't need to edit these in the main webserver application. If you ever need to login into the MySQL server then use these credentitals. If you change the database value from shuttle
then you will also have to edit the sql setup_db.sql file to match this new value. Better just leaving that the way it is.  

### Generate Local SSL Certificates
Run the following command on the terminal and copy the certificates into the ./data/certs folder. The docker image will mount this directory and expose this to the node server for running locally.  
These certificates should be replaced with LetsEncrypt, or equivalent, certificates when running the server in production. 
