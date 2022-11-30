# Make sure the image of lab1 was built in your ACR
ARG BASE_IMAGE
FROM $BASE_IMAGE
RUN '(Invoke-RestMethod -Method GET -Uri "http://www.boredapi.com/api/activity/").activity -split " " | Write-Ascii' > entrypoint.ps1