# Create Group Variable:
$group = Get-MgGroup | Where-Object {$_.DisplayName -eq "Contoso_Sales"}

# Create Group Variable:
$user = Get-MgUser | Where-Object {$_.DisplayName -eq "Cody Godinez"}

# Adding User to group
New-MgGroupMember -GroupId $group.Id -DirectoryObjectId $user.Id

# Verify that user added:
Get-MgGroupMember -GroupId $group.Id | FL