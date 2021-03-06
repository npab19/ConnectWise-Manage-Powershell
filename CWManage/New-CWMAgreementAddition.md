# New-CWMAgreementAddition
## SYNOPSIS
This function will create a new agreement addition.
## SYNTAX
```powershell
New-CWMAgreementAddition [-AgreementID] <Int32> [[-id] <Int32>] [-product] <Object> [[-quantity] <Single>] [[-lessIncluded] <Single>] [[-unitPrice] <Single>] [[-unitCost] <Single>] [-billCustomer] <Object> [[-effectiveDate] <String>] [[-cancelledDate] <String>] [[-taxableFlag] <Boolean>] [[-serialNumber] <String>] [[-invoiceDescription] <String>] [[-purchaseItemFlag] <Boolean>] [[-specialOrderFlag] <Boolean>] [[-description] <String>] [[-billedQuantity] <Single>] [[-uom] <String>] [[-extPrice] 

<Single>] [[-extCost] <Single>] [[-sequenceNumber] <Single>] [[-margin] <Single>] [[-prorateCost] <Single>] [[-proratePrice] <Single>] [[-extendedProrateCost] <Single>] [[-extendedProratePrice] <Single>] [[-prorateCurrentPeriodFlag] <Boolean>] [[-_info] <Object>] [<CommonParameters>]
```
## PARAMETERS
### -AgreementID &lt;Int32&gt;

```
Required                    true
Position                    1
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -id &lt;Int32&gt;

```
Required                    false
Position                    2
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -product &lt;Object&gt;

```
Required                    true
Position                    3
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -quantity &lt;Single&gt;

```
Required                    false
Position                    4
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -lessIncluded &lt;Single&gt;

```
Required                    false
Position                    5
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -unitPrice &lt;Single&gt;

```
Required                    false
Position                    6
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -unitCost &lt;Single&gt;

```
Required                    false
Position                    7
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -billCustomer &lt;Object&gt;

```
Required                    true
Position                    8
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -effectiveDate &lt;String&gt;

```
Required                    false
Position                    9
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -cancelledDate &lt;String&gt;

```
Required                    false
Position                    10
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -taxableFlag &lt;Boolean&gt;

```
Required                    false
Position                    11
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -serialNumber &lt;String&gt;

```
Required                    false
Position                    12
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -invoiceDescription &lt;String&gt;

```
Required                    false
Position                    13
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -purchaseItemFlag &lt;Boolean&gt;

```
Required                    false
Position                    14
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -specialOrderFlag &lt;Boolean&gt;

```
Required                    false
Position                    15
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -description &lt;String&gt;

```
Required                    false
Position                    16
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -billedQuantity &lt;Single&gt;

```
Required                    false
Position                    17
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -uom &lt;String&gt;

```
Required                    false
Position                    18
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -extPrice &lt;Single&gt;

```
Required                    false
Position                    19
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -extCost &lt;Single&gt;

```
Required                    false
Position                    20
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -sequenceNumber &lt;Single&gt;

```
Required                    false
Position                    21
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -margin &lt;Single&gt;

```
Required                    false
Position                    22
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -prorateCost &lt;Single&gt;

```
Required                    false
Position                    23
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -proratePrice &lt;Single&gt;

```
Required                    false
Position                    24
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -extendedProrateCost &lt;Single&gt;

```
Required                    false
Position                    25
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -extendedProratePrice &lt;Single&gt;

```
Required                    false
Position                    26
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -prorateCurrentPeriodFlag &lt;Boolean&gt;

```
Required                    false
Position                    27
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -_info &lt;Object&gt;

```
Required                    false
Position                    28
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>$CreateParam = @{

AgreementID = $Agreement.id
    product = @{id = $Product.id}
    billCustomer = 'DoNotBill'
    quantity = $Quantity
    taxableFlag = $true
    effectiveDate = $(Get-Date (Get-Date -Day 1).AddMonths(1) -format yyyy-MM-ddTHH:mm:ssZ)
}
New-CWMAgreementAddition @CreateParam
```

## NOTES
Author: Chris Taylor

Date: 4/2/2018 
## LINKS
http://labtechconsulting.com

https://developer.connectwise.com/manage/rest?a=Finance&e=AgreementAdditions&o=CREATE
