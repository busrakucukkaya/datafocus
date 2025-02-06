## Docker Installation for Linux

### System Requirements
Docker Engine installation steps vary depending on the Linux distribution.

### Steps to Install Docker
1. Refer to the [Official Docker Documentation](https://docs.docker.com/engine/install/) for distro-specific installation instructions.
2. Use the package manager of your Linux distribution to install Docker.
   - **Recommended version:** Docker Engine 26 or higher.


---

## Docker Installation for Windows

### System Requirements
- **WSL Version:** 1.1.3.0 or later.
- **Operating System:** Windows Server 2022 (build 20348) or higher is recommended.

### Steps to Install Docker
1. **Activate the WSL 2 feature on Windows.**
   - For detailed guidance, refer to the [Microsoft WSL Documentation](https://learn.microsoft.com/en-us/windows/wsl/install).

#### Hardware Prerequisites for WSL 2
1. A 64-bit processor with **Second Level Address Translation (SLAT)** support is required.
    - **Hardware virtualization (Nested Virtualization)** must be enabled in your system’s BIOS settings. For further details, check the [Virtualization Overview](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/).

2. **Once WSL 2 is enabled, download and install Docker.**
    - We recommend **Docker Desktop 4.34.2** for enhanced security and performance. It can be downloaded from [Docker Desktop 4.34.2](https://docs.docker.com/desktop/release-notes/).

3. **To run Data Focus, allocate at least:**
    - 32 GiB memory
    - 8 vCPUs

   **To modify these settings:**

- Open **Docker Desktop**.
- Navigate to **Preferences > Resources > Advanced**.
- Adjust **memory and CPU** allocation as required.

---

## Verify Docker Installation
To check the installed Docker version, run the following command:

```zsh
docker version
```
!!! warning 
    If you need to install Docker offline, please contact with product.devops@kafein.com.tr