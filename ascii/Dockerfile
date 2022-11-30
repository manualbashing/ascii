FROM mcr.microsoft.com/powershell:latest
SHELL ["pwsh", "-c"]
RUN Set-PSRepository -Name 'PSGallery' -InstallationPolicy Trusted; Install-Module -Name WriteAscii
# Bugfix for missing cmdlet alias in PowerShell Core
RUN New-Item $PROFILE -Force; "New-Alias Sort Sort-Object" >> $PROFILE
RUN 'Write-Ascii "$args"' >> entrypoint.ps1
ENTRYPOINT ["pwsh", "entrypoint.ps1"]
CMD ["The winner is: 4610"]