# Add-On Kafka Stack

This stack uses the `database-stack_default network` to connect with the `database-stack` using docker service names DNS resolution.

Default usage requires the `database-stack` to have already been launched.  

> To use without the `database-stack`, comment out the __networks__ section of the `docker-compose.yml` file.

### Usage

Copy the `.env.sample` file to `.env` and adjust the settings as required:

```
CDK_ADMIN_EMAIL="admin@admin.io"
CDK_ADMIN_PASSWORD="admin"

POSTGRES_USER=postgres
POSTGRES_PASSWORD=Password123
```

`bash launch-stack.sh`

or

```
docker-compose -p "kafka-stack" up -d
```

## Conduktor

Connect to the `conduktor` management UI at `localhost:8080` to manage the Kafka cluster.  Use the CDK_ADMIN_EMAIL and CDK_ADMIN_PASSWORD supplied in the `.env` file.
