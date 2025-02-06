You will receive a .tar.gz package, such as datafocus-2.0.0.tar.gz. Follow these steps to extract it:

!!! Abstract ""
    === "Linux"
        ```bash
        mkdir datafocus
        tar -xvzf datafocus-2.0.0.tar.gz -C path/to/your/datafocus  
        ```

    === "Windows"
        ```powershell
        New-Item -ItemType Directory -Name "datafocus"
        tar -xvzf datafocus-2.0.0.tar.gz -C path/to/your/datafocus  
        ```

!!! info "Windows Server 2022 and higher releases includes ```tar``` built-in. "