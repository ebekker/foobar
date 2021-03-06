---
external help file: ACMESharp.POSH.dll-Help.xml
online version: 
schema: 2.0.0
---

# Update-ACMEIdentifier

## SYNOPSIS
Updates the status and details of an Identifier stored in the Vault.

## SYNTAX

### Default (Default)
```
Update-ACMEIdentifier [-IdentifierRef] <String> [-UseBaseUri] [-NewAlias <String>] [-Label <String>]
 [-Memo <String>] [-VaultProfile <String>]
```

### Challenge
```
Update-ACMEIdentifier [-IdentifierRef] <String> [-ChallengeType] <String> [-UseBaseUri] [-NewAlias <String>]
 [-Label <String>] [-Memo <String>] [-VaultProfile <String>]
```

### LocalOnly
```
Update-ACMEIdentifier [-IdentifierRef] <String> [-LocalOnly] [-NewAlias <String>] [-Label <String>]
 [-Memo <String>] [-VaultProfile <String>]
```

## DESCRIPTION
Use this cmdlet to update characteristics of an Identifier that are defined locally, such as the Alias or Label.

Also use this cmdlet to refresh the state and status of an Identifier by probing the associated ACME CA Server for Identifier details.

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -IdentifierRef
A reference (ID or alias) to a previously defined Identifier submitted to the ACME CA Server for verification.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ref

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ChallengeType
Specifies the ACME Challenge type that should be updated.

```yaml
Type: String
Parameter Sets: Challenge
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBaseUri
Overrides the base URI associated with the target Registration and used for subsequent communication with the associated ACME CA Server.

```yaml
Type: SwitchParameter
Parameter Sets: Default, Challenge
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalOnly
Indicates that updates should be performed locally only, and no attempt should be made to retrieve the current status from the ACME CA Server.

```yaml
Type: SwitchParameter
Parameter Sets: LocalOnly
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewAlias
Optionaly, set or update the unique alias assigned to the Identifier for future reference.
To remove the alias, use the empty string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Label
Optionally, set or update the human-friendly label to assigned to the Identifier for easy recognition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Memo
Optionall, set or update the arbitrary text field used to capture any notes or details associated with the Identifier.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultProfile
Specifies a Vault profile name that will resolve to the Vault instance to be used for all related operations and storage/retrieval of all related assets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-Identifier]()

[Get-Identifier]()

[Complete-Challenge]()

[Submit-Challenge]()

