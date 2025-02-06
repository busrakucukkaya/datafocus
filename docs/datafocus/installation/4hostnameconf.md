title: Hostname Configuraiton
Since Data Focus is a client-side application, hostname parameters must be configured for each service. 

  Run the following command:
!!! Abstract "Provide the appropriate hostname (an IP address or DNS name). This hostname must be the VM's IP address or a DNS, as it will be the address through which the application is accessed. "

!!! Abstract ""
    === "Linux"
        ```bash
        ./config.sh set_hostname  
        ```

    === "Windows"
        ```powershell
        ./config.ps1 set_hostname 
        ```  
!!! warning "If you use a DNS address as the hostname, ensure that you have valid certificates to enable HTTPS."