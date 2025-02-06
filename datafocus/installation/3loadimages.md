After extracting the tar.gz package, it needs to be loaded. These compressed Docker images are created using the docker save command, with compression reducing the package size by over 70%.

To load the Docker images:


!!! Abstract ""
    === "Linux"
        ```bash
        ./config.sh load_images
        ```

    === "Windows"
        ```powershell
        ./config.ps1 load_images
        ```

To verify the imported images using:

!!! Abstract ""
    === "Linux"
        ```bash
        docker image ls  
        ```

    === "Windows"
        ```powershell
        docker image ls  
        ```  
