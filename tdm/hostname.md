The `set_hostname` script is a utility provided with the application to help configure the necessary hostname parameters. This script sets up the appropriate settings for the frontend, backend, and CORS (Cross-Origin Resource Sharing) configurations.

The `set_hostname` script specifically sets the browser URL for the application. This includes configuring the protocol (e.g., HTTP or HTTPS) and the domain name which helps us using any port on the URL. Ensuring the correct browser URL is essential for users to access the application through their web browsers and for the application to properly handle requests and responses.

!!! Abstract "You will need the following variable when the running script."
    - Hostname (Ip or DNS)

    !!! Abstract ""
        === "Linux"
            ```bash
            ./config.sh set_hostname
            ```

        === "Windows"
            ```powershell
            ./config.ps1 set_hostname
            ```

