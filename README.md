# Strapi Plesk Application

Demo project to this [blog post](https://raoulkramer.de/deploy-run-host-strapi-on-plesk-obsidian-as-node-application) to run a strapi application on a plesk vserver as [nodejs application](./server.js).

## quickstart sqlite

* clone repository
* copy [`.env.example`](./.env.example) to `.env`
* add `DATABASE_CONNECTION_NAME=sqlite`
* add JWT secrets by running this node command: node -e "console.log(require('crypto').randomBytes(64).toString('base64'))"

## quickstart mysql

* clone repository
* copy [`.env.example`](./.env.example) to `.env`
* add `DATABASE_CONNECTION_NAME=mysql`
* provide values for other `DATABASE_*` fields (NAME, USERNAME, PASSWORD, HOST, PORT)
* add JWT secrets by running this node command: node -e "console.log(require('crypto').randomBytes(64).toString('base64'))"

## quickstart jwt secrets

Provide two different jwt secret values in your `.env` file.

Create `JWT_SECRET` and `ADMIN_JWT_SECRET` value with this command:

```bash
node -e "console.log(require('crypto').randomBytes(64).toString('base64'))"
```
