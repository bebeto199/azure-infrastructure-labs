# Lab 01 - Domain Controller in Azure

## Objective
Deploy Windows Server and promote it to a Domain Controller.

## Steps

1. Create Azure VM (Windows Server 2022)
2. Assign static private IP
3. Install AD DS role:

```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

4. Promote to domain controller:

```powershell
Install-ADDSForest -DomainName "corp.local"
```

5. Validate:

```powershell
Get-ADUser
```

## Outcome
- Active Directory deployed successfully in Azure
