## Generate Synapse Config

Run the following command to generate the initial Synapse configuration:

```bash
docker compose run --rm \
  -e SYNAPSE_SERVER_NAME=matrix.domen.com \
  -e SYNAPSE_REPORT_STATS=yes \
  synapse generate
```

## Create Admin User

Enter the Synapse container and create an admin account:

```bash
docker exec -it synapse bash
register_new_matrix_user -u admin -p admin -a -c /data/homeserver.yaml
```
