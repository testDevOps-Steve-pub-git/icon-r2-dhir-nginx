# dhir-nginx

This repo contains the files for creating outbound connection from `ICON` to `DHIR` server using mutual authentication

### Things to do before deploying Cloud Foundry app: -

 - Replace the certificates in `SSL` folder
 - Updated the `DHIR server name` and `certificates name` in `public/nginx.conf` file

### SSL files need for Mutual Authentication between `ICON` and `DHIR`

 - Certificate file
 - Certificate key file
 - Trusted/Root Certificate file

### Steps to deploy DHIR-NGINX server to Bluemix using Cloud Foundry: -

 - Install cloud foundry command line interface from https://github.com/cloudfoundry/cli/releases
 - Set the Cloud Foundry to point to Bluemix
    #### ``` cf api https://api.ng.bluemix.net ```
 - Login to the Bluemix. Replace the username, organization and space value
    #### ``` cf login -u ravi.chaudhary@mohawkcollege.ca -o "ICON R2" -s dev ```

    Options available for space in `Mohawk Bluemix account`: -
    - `dev`
    - `staging`


 - Push to Bluemix
    #### ``` cf push -f bluemix/dev-manifest.yml```

    Options available for manifest: -
    - `dev-manifest.yml`
    - `stg-manifest.yml`
