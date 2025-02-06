# Keycloak Configuration

Keycloak serves as the Identity and Access Management (IAM) solution for Data Focus. It offers Single Sign-On (SSO) features, user management, and role-based access control (RBAC).

> **NOTE:** After deployment, the login screen will not be accessible due to Keycloak restrictions. To resolve this, log in to Keycloak and update the client configurations for Data Focus.

## HTTPS Configuration

If your setup uses HTTPS, you must update the Keycloak service configuration in the `docker-compose.yml` file. Follow these steps:

**1.** Open the `docker-compose.yml` file with a text editor.

**2.** Locate the Keycloak service configuration block.

**3.** Update the command block as shown below:

   ```yaml
   command: start --import-realm
   ```
**4.** Update the `KC_HOSTNAME` and `KC_PROXY` environment variables to your hostname and uncomment the HTTPS-related lines in the configuration. Save the changes and restart the service.

## Client Configurations

To configure the client settings:

**1. Access Keycloak:** Open your browser and navigate to:
   ```
   http://<hostname>/auth
   ```
**2. Login Credentials:** 

- **Username:** `admin-demo`
- **Password:** `admin-demo`


**3. Switch to DataFocus Realm:**

- In the upper-left menu, ensure you are in the **Keycloak** realm.

- The DataFocus realm is imported automatically when Keycloak starts. Click on **DataFocus** to switch to this realm.

**4. Update Client Configuration:**

- Navigate to **Clients** in the left menu.
- Find the `datafocusId` client and update the following fields:
        
        - **Root URL:** Set this to your hostname.
        - **Valid Redirect URIs:** Update to include the hostname.
     
     **Example configuration:**
     
     ```
     Root URL: https://<hostname>
     Valid Redirect URIs: https://<hostname>/*
     ```
  
**5. Save the changes and verify the configuration.**
