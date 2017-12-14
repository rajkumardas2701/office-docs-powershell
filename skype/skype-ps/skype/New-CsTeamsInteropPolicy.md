---
external help file: tmp_etapwmkb.i42-help.xml
Module Name: tmp_etapwmkb.i42
online version: 
schema: 2.0.0
---

# New-CsTeamsInteropPolicy

## SYNOPSIS
Determines how calls are routed between Skype for Business and Microsoft Teams. This cmdlet s typically used by organizations that have users on both Skype for Business and Microsoft Teams and want to configure how calls are handled in their organization.

**Note**: This document is provided for early evaluation of Calling Plans support for Microsoft Teams. TeamsInteropPolicy does not currently respect the policy’s chat settings and the current implementation may change in the future.

New-CsTeamsInteropPolicy \[-Identity\] \<XdsIdentity\> \[-Tenant \<guid\>\] \[-AllowEndUserClientOverride \<bool\>\] \[-CallingDefaultClient \<string\>\] \[-ChatDefaultClient \<string\>\] \[-InMemory\] \[-Force\] \[-WhatIf\] \[-Confirm\] \[\<CommonParameters\>\]

## SYNTAX

```
New-CsTeamsInteropPolicy [-Force] [-WhatIf] [-AllowEndUserClientOverride <Object>] [-Confirm]
 [[-Identity] <Object>] [-Tenant <Object>] [-InMemory] [-ChatDefaultClient <Object>]
 [-CallingDefaultClient <Object>] [-AsJob]
```

## DESCRIPTION
Interoperability (interop for short) enables Skype for Business and Teams users to chat and call with one another, ensuring that communications remain fluid across your organization. 
This policy helps IT pros manage the adoption of Teams by determining how to route calls across apps and whether to enable users to choose which app to use for calling. 
Teams interop policy can be defined at the tenant or per-user level.

Teams interop policy can be configured to keep voice communications in Teams and Skype for Business siloed, or it can be configured to enable users to communicate across application boundaries.

For comprehensive documentation on this policy and it’s settings, see [Microsoft Teams and Skype for Business Interoperability](https://docs.microsoft.com/MicrosoftTeams/teams-and-skypeforbusiness-interoperability).

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AllowEndUserClientOverride
{{Fill AllowEndUserClientOverride Description}}

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CallingDefaultClient
{{Fill CallingDefaultClient Description}}

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ChatDefaultClient
{{Fill ChatDefaultClient Description}}

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
{{Fill Force Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
{{Fill Identity Description}}

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InMemory
{{Fill InMemory Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
{{Fill Tenant Description}}

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

**External Calling Support**
Calls from external callers on PSTN is only available for users who have been provisioned with a Calling Plan.

**Supported Topologies**
Interoperability between Teams and Skype for Business is supported between users who are purely online (Skype for Business Online and Teams), and users homed in a Skype for Business on-premises deployment in a mixed (Hybrid) deployment topology.

**Hybrid Voice is not supported at this time**
Interop support for Skype for Business Hybrid does not include Hybrid Voice capabilities delivered through CCE (Cloud Connector Edition) or on-premises PSTN connectivity using existing deployment--or commonly called as OPCH (On Prem Config Hybrid). 
Teams users cannot be enabled for PSTN calling capabilities using CCE or OPCH.

**IP Phone Support**
Currently, changing CallingDefaultClient to Teams will also affect calls to Skype for Business IP phones. 
Incoming calls will not be received on the phones and will only ring Teams clients. 
Please consult the [Skype for Business to Microsoft Teams Capabilities Roadmap](https://aka.ms/skype2teamsroadmap) for information about support for existing certified SIP phones.


## RELATED LINKS

[Skype for Business to Microsoft Teams Capabilities Roadmap](https://aka.ms/skype2teamsroadmap)

[Microsoft Teams and Skype for Business Interoperability](https://docs.microsoft.com/MicrosoftTeams/teams-and-skypeforbusiness-interoperability)