# Use Windows Nano Server base image
FROM mcr.microsoft.com/windows/nanoserver:ltsc2022

# Set working directory
WORKDIR C:\gotohp

# Download gotohp-cli.exe
ADD https://github.com/xob0t/gotohp/releases/latest/download/gotohp-cli-x64.exe C:\gotohp\gotohp-cli.exe

# Make sure PowerShell can run scripts
SHELL ["powershell", "-Command"]

# Copy entrypoint script
COPY entrypoint.ps1 C:\gotohp\entrypoint.ps1

# Set entrypoint
ENTRYPOINT ["C:\\gotohp\\entrypoint.ps1"]
