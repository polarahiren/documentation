# Fixing Laravel Echo Server

### Things to make sure

- Make sure you configured `keyPrefix` for redis database. If you have multiple instances of echo server running on
  server having same `keyPrefix` then it will misbehave.

```json
{
  "databaseConfig": {
    "redis": {
      "keyPrefix": "example_database_"
    }
  }
}
```
- Make sure `sslCertPath` and `sslKeyPath` are setup correctly.
- Use different port if you are having multiple instance running on same server.

### If it doesn't work
> If echo server is running and you see requests failing in network tab under developer console.

1. Try to restart Daemon service from Forge and see if it makes echo server working.
2. Check to see if SSL certificate and key path is correct. LetsEncrypt is renewing licence auto on forge server, so old certificate path won't work with echo server.
    - Example of SSL path `/etc/nginx/ssl/example.com/966304/server.crt`
    - Go to SSL directory by executing `cd /etc/nginx/ssl/example.com`
    - Replace the latest directory number you see in path.
    - Restart Daemon from Forge.
3. Stop the Daemon service from Forge and do the following:
    - SSH into server 
    - Go to your site
    - Open `laravel-echo-server.json` and set `devMode: true`
    - Run `laravel-echo-server start` manually in terminal
    - Refresh your site in browser and see the errors in terminal.
