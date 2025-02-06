Once the configuration is complete, you can deploy the Data Focus application.

### Starting the Data Focus

1. **Verify Compose Services**  
   Before running the application, ensure all Docker Compose services are correctly configured.

2. **Start Services**  
   Run the following command to start the application:
   ```sh
   docker compose up -d
   ```
   This command will bring all containers online. Verify that all containers are in a healthy state. 
3. **Troubleshooting Unhealthy Containers**  
   If a container is in an unhealthy state, inspect its logs to identify the issue:
   ```sh
   docker logs -f <servicename> --tail=1000
   ```
   Once all containers are running and healthy, proceed to sections **Keycloak Configuration** and **MinIO Configuration** for further configuration.