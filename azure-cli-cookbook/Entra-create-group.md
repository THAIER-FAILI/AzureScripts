# Login:
Connect-MgGraph -scopes "user.readwrite.all, group.readwrite.all"

# Create a new group
New-MgGroup -DisplayName "Contoso_Sales" -Description "Contoso Sales team users" -MailEnabled:$false -Mailnickname "Contoso_Sales" -SecurityEnabled

# Verify Groups:
Get-MgGroup

