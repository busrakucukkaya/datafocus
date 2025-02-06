
# HTTPS Configuration (Optional)

By default, the setup uses HTTP, but it can easily be switched to HTTPS. The router is pre-configured to enable HTTPS. Before proceeding, ensure the following prerequisites are met:

- **DNS A Records**: Properly configured DNS A records pointing to your server's IP address.
- **SSL Certificates**: To enable HTTPS, you need:
  - A valid SSL certificate (`.crt` file).
  - The corresponding SSL certificate key (`.key` file).

If you inspect the `router.conf` file under the router directory, you'll find pre-configured lines for HTTPS that are commented out.
# Steps to Enable HTTPS

## 1. Place the Certificates
Copy your certificate files (.crt and .key) to the router directory.

## 2. Edit `default.conf`
Open the `default.conf` file in a text editor. Uncomment the pre-configured HTTPS lines by removing the `#` at the beginning. Comment out any unnecessary HTTP lines by adding a `#` at the start of the line.

## 3. Update SSL Certificate Paths
Update the `ssl_certificate` and `ssl_certificate_key` paths in the `default.conf` file to match the names and locations of the certificate files you placed in the router directory. For example:

```
ssl_certificate /etc/nginx/conf.d/example.crt;
ssl_certificate_key /etc/nginx/conf.d/example.key;
```

## 4. Restart the Router
After making these changes, restart the router service using the following command:

```bash
docker compose restart router
```

## 5. Update Hostname Configuration
After switching to HTTPS, some applications may require reconfiguration. Set the hostname according to your DNS address. Refer to the **Hostname Configuration** section for details.

## 6. Update Keycloak Configuration
Update the `datafocusId` client in Keycloak. Follow the instructions in the **Keycloak Configurations** section to complete the update.

Once these configurations are complete, you can access Data Focus over HTTPS at:

```
https://<hostname>
```
