# ConnectWise Manage PowerShell REST API Wrapper
This is a PowerShell wrapper for the ConnectWise Manage REST API.

https://developer.connectwise.com/Products/Manage/REST

The simplest way to connect is with your Manage username and password.
```
# Import the module
iwr 'https://raw.githubusercontent.com/LabtechConsulting/ConnectWise-Manage-Powershell/master/CWManage.psm1' | iex

# Create a [pscredential] object
$Password = ConvertTo-SecureString -AsPlainText -Force $PlainTextPassword
$Credentials = New-Object PSCredential $UserName, $Password

# Set our connection parameters
$Connection = @{
    Server = $Server
    Company = $Company
    Credentials = $Credentials
}

# Connect to Manage server
Connect-CWM @Connection
```
This will cache the connection info to memory for subsequent commands to use.
```
# Find all the cool people
$Chrises = Get-CWMContact -condition 'firstName="chris"' -all
```
Once you are completed with your tasks you can clear the connection info from memory.
```
# Clear connection information from memory
Disconnect-CWM
```

See below for a list of available commands.
# Functions

[Connect-CWM](CWManage/Connect-CWM.md)

[ConvertFrom-CWMColumnRow](CWManage/ConvertFrom-CWMColumnRow.md)

[ConvertFrom-CWMTime](CWManage/ConvertFrom-CWMTime.md)

[ConvertTo-CWMTime](CWManage/ConvertTo-CWMTime.md)

[Disconnect-CWM](CWManage/Disconnect-CWM.md)

[Get-CWMAgreement](CWManage/Get-CWMAgreement.md)

[Get-CWMAgreementAddition](CWManage/Get-CWMAgreementAddition.md)

[Get-CWMAuditTrail](CWManage/Get-CWMAuditTrail.md)

[Get-CWMBoardStatus](CWManage/Get-CWMBoardStatus.md)

[Get-CWMChargeCode](CWManage/Get-CWMChargeCode.md)

[Get-CWMCompany](CWManage/Get-CWMCompany.md)

[Get-CWMCompanyConfiguration](CWManage/Get-CWMCompanyConfiguration.md)

[Get-CWMCompanyStatus](CWManage/Get-CWMCompanyStatus.md)

[Get-CWMCompanyTeam](CWManage/Get-CWMCompanyTeam.md)

[Get-CWMCompanyTeamRole](CWManage/Get-CWMCompanyTeamRole.md)

[Get-CWMCompanyType](CWManage/Get-CWMCompanyType.md)

[Get-CWMCompanyTypeAssociation](CWManage/Get-CWMCompanyTypeAssociation.md)

[Get-CWMContact](CWManage/Get-CWMContact.md)

[Get-CWMDocument](CWManage/Get-CWMDocument.md)

[Get-CWMManufacturer](CWManage/Get-CWMManufacturer.md)

[Get-CWMMembers](CWManage/Get-CWMMembers.md)

[Get-CWMProduct](CWManage/Get-CWMProduct.md)

[Get-CWMProductCatalog](CWManage/Get-CWMProductCatalog.md)

[Get-CWMProductComponent](CWManage/Get-CWMProductComponent.md)

[Get-CWMProductSubCategory](CWManage/Get-CWMProductSubCategory.md)

[Get-CWMProductType](CWManage/Get-CWMProductType.md)

[Get-CWMProject](CWManage/Get-CWMProject.md)

[Get-CWMProjectPhase](CWManage/Get-CWMProjectPhase.md)

[Get-CWMProjectSecurityRole](CWManage/Get-CWMProjectSecurityRole.md)

[Get-CWMProjectTeamMember](CWManage/Get-CWMProjectTeamMember.md)

[Get-CWMReport](CWManage/Get-CWMReport.md)

[Get-CWMReportColumn](CWManage/Get-CWMReportColumn.md)

[Get-CWMScheduleEntry](CWManage/Get-CWMScheduleEntry.md)

[Get-CWMServiceBoard](CWManage/Get-CWMServiceBoard.md)

[Get-CWMSystemInfo](CWManage/Get-CWMSystemInfo.md)

[Get-CWMTicket](CWManage/Get-CWMTicket.md)

[Get-CWMTicketConfiguration](CWManage/Get-CWMTicketConfiguration.md)

[Get-CWMTicketNote](CWManage/Get-CWMTicketNote.md)

[Invoke-CWMAllResult](CWManage/Invoke-CWMAllResult.md)

[Invoke-CWMDeleteMaster](CWManage/Invoke-CWMDeleteMaster.md)

[Invoke-CWMGetMaster](CWManage/Invoke-CWMGetMaster.md)

[Invoke-CWMNewMaster](CWManage/Invoke-CWMNewMaster.md)

[Invoke-CWMPatchMaster](CWManage/Invoke-CWMPatchMaster.md)

[Invoke-CWMSearchMaster](CWManage/Invoke-CWMSearchMaster.md)

[Invoke-CWMWebRequest](CWManage/Invoke-CWMWebRequest.md)

[New-CWMAgreementAddition](CWManage/New-CWMAgreementAddition.md)

[New-CWMCompanyTeam](CWManage/New-CWMCompanyTeam.md)

[New-CWMCompanyTypeAssociation](CWManage/New-CWMCompanyTypeAssociation.md)

[New-CWMContact](CWManage/New-CWMContact.md)

[New-CWMProductCatalog](CWManage/New-CWMProductCatalog.md)

[New-CWMProjectTeamMember](CWManage/New-CWMProjectTeamMember.md)

[New-CWMScheduleEntry](CWManage/New-CWMScheduleEntry.md)

[New-CWMTicket](CWManage/New-CWMTicket.md)

[Remove-CWMCompanyConfiguration](CWManage/Remove-CWMCompanyConfiguration.md)

[Remove-CWMCompanyTypeAssociation](CWManage/Remove-CWMCompanyTypeAssociation.md)

[Remove-CWMScheduleEntry](CWManage/Remove-CWMScheduleEntry.md)

[Remove-CWMTicket](CWManage/Remove-CWMTicket.md)

[Update-CWMAgreementAddition](CWManage/Update-CWMAgreementAddition.md)

[Update-CWMCompany](CWManage/Update-CWMCompany.md)

[Update-CWMCompanyTypeAssociation](CWManage/Update-CWMCompanyTypeAssociation.md)

[Update-CWMProductCatalog](CWManage/Update-CWMProductCatalog.md)

[Update-CWMProjectPhase](CWManage/Update-CWMProjectPhase.md)

[Update-CWMTicket](CWManage/Update-CWMTicket.md)


