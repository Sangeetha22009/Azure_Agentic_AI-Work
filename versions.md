echo # Installed Tool Versions > versions.md
for /f "delims=" %i in ('az version --query azureCliVersion -o tsv') do echo Azure CLI: %i >> versions.md
azd version >> versions.md
for /f "delims=" %i in ('az bicep version') do echo Bicep: %i >> versions.md
