# Mattermost on Coolify

This is a docker compose file to get mattermost running on coolify based on this discussion here: https://github.com/coollabsio/coolify/discussions/3087#discussion-7053964

## Intrusctions:

1. Set up a new service using this compose file.
2. Once the service is set up, but before deploying it, make sure to change the url. One can be automatically assigned if you have a wildcard domain setup for the coolify server.
3. You will need to run this command as root on the server where the service will be deployed:

```bash
sudo chown -R 2000:2000 bleve-indexes/ client/ config/ data/ logs plugins
```

   The disccussion mentions to run this in `/data/coolify/services/SERVICE_ID` but I had to do it in `/data/coolify/applications/SERVICE_ID`. You may need to create the folders in question.

4. Deploy the service and check if everything is working as expected. (The mattermost container may require a few minutes to start up)
