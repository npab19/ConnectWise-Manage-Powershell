# Invoke-CWMGetMaster
## SYNOPSIS
This will be basis of all get calls to the ConnectWise Manage API.
## SYNTAX
```powershell
Invoke-CWMGetMaster [[-Arguments] <Object>] [[-URI] <String>] [<CommonParameters>]
```
## DESCRIPTION
This will insure that all GET requests are handled correctly.
## PARAMETERS
### -Arguments &lt;Object&gt;
A hash table of parameters
```
Required                    false
Position                    1
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -URI &lt;String&gt;
The URI of the GET endpoint
```
Required                    false
Position                    2
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>Invoke-CWMGetMaster -Arguments $Arguments -URI $URI
```

## NOTES
Author: Chris Taylor

Date: 10/10/2018 
## LINKS
http://labtechconsulting.com

https://developer.connectwise.com/Manage/Developer_Guide#Authentication
