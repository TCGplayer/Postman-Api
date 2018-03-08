# Postman-Api
This repository contains two files.  The first, TCGPlayer.postman_collection.json, is a Postman (https://www.getpostman.com) collection file that contains all of the current API requests.  The second file, TCGPlayer.postman_environment, contains a set of environment variables that will need to be set and configured to get the collection to work.

First you will need to import both of these files into Postman.  After that is done, modify the environment variables to match your credentials.  The ones that need to be modified are:
publicId- this is the public key that you were given when receiving API access
privateId- this is the private key that you were given when receiving API access

The rest of the fields will populate from scripts through the various requests.  storeAuthorizationCode is part of the Store Authorization workflow present in the [main documentation](https://docs.tcgplayer.com/docs/store-authorization-workflow).

# Getting started with TCGPlayer Postman requests
After your keys are entered into the imported environment, there are two paths to follow depending on if you want to authenticate against a store.  This is only necessary if your application will be interacting with store objects, such as by pulling a store's orders.

If you don't want to authenticate against a store, skip to step 4.

###1)
Follow the [store authorization workflow](https://docs.tcgplayer.com/docs/store-authorization-workflow) until you have generated a store's authorization code.
###2)
Enter this code into your Postman environment under the storeAuthorizationCode variable.
###3)
Run the request for Store Authorization.  You don't need to copy anything from the response, the script handles it and loads the appropriate environment variables.
###4)
Run the request for Authenticate.

After this is completed, you should be able to start diving in and running any of the other requests in the collection.  If you authenticated against a store, a great next step is to call Get Store Info so that you can verify that your store's information is returned correctly.

# Notes
This postman collection is currently updated for version 1.9.0 of the TCGPlayer API.  When new version come out, this section will be updated and the collection will also be updated.

If you have any questions please feel free to reach out on our [community forums](https://community.tcgplayer.com)!




Repository published by Joshua Burdick, Developer Evangelist at TCGPlayer.com
