# Login:
Connect-MgGraph -scopes "user.readwrite.all, group.readwrite.all"

# Creat Password Profile:
  $PWProfile = @{
      Password = "Pa55w.rd";
      ForceChangePasswordNextSignIn = $false
  }

# Create User:
    New-MgUser `
      -DisplayName "Cody Godinez" `
      -GivenName "Cody" -Surname "Godinez" `
      -MailNickname "cgodinez" `
      -UsageLocation "US" `
      -UserPrincipalName "cgodinez@M365x18886398.onmicrosoft.com" `
      -PasswordProfile $PWProfile -AccountEnabled `
      -Department "Sales" -JobTitle "Sales Rep"

Verify users in Entra
Get-MgUser    