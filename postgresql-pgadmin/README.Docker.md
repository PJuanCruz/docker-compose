### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

---

### Connect PgAdmin4:

- Login:

  - Email Address / Username: [PGADMIN_DEFAULT_EMAIL]
  - Password: [PGADMIN_DEFAULT_PASSWORD]

    Login

Servers > Register > Server...

- General:
  - Name: PostgreSQL

* Connection:

  - Host name/address: [service name (postgresql)]
  - Port: 5432
  - Username: [POSTGRES_USER]
  - Password: [POSTGRES_PASSWORD]

  Save
