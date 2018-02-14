---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Set-MailPublicFolder

## SYNOPSIS
!!! Exchange Server 2010

Use the Set-MailPublicFolder cmdlet to configure the mail-related settings of mail-enabled public folders. If you want to configure basic settings that aren't mail related, use the Set-PublicFolder cmdlet.

!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Set-MailPublicFolder cmdlet to configure the mail-related settings of mail-enabled public folders. If you want to configure basic settings that aren't mail related, use the Set-PublicFolder cmdlet.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Set-MailPublicFolder [-Identity] <MailPublicFolderIdParameter> [-AcceptMessagesOnlyFrom <MultiValuedProperty>]
 [-AcceptMessagesOnlyFromDLMembers <MultiValuedProperty>]
 [-AcceptMessagesOnlyFromSendersOrMembers <MultiValuedProperty>] [-Alias <String>]
 [-ArbitrationMailbox <MailboxIdParameter>] [-BypassModerationFromSendersOrMembers <MultiValuedProperty>]
 [-Confirm] [-Contacts <RecipientIdParameter[]>] [-CreateDTMFMap <$true | $false>] [-CustomAttribute1 <String>]
 [-CustomAttribute10 <String>] [-CustomAttribute11 <String>] [-CustomAttribute12 <String>]
 [-CustomAttribute13 <String>] [-CustomAttribute14 <String>] [-CustomAttribute15 <String>]
 [-CustomAttribute2 <String>] [-CustomAttribute3 <String>] [-CustomAttribute4 <String>]
 [-CustomAttribute5 <String>] [-CustomAttribute6 <String>] [-CustomAttribute7 <String>]
 [-CustomAttribute8 <String>] [-CustomAttribute9 <String>] [-DeliverToMailboxAndForward <$true | $false>]
 [-DisplayName <String>] [-DomainController <Fqdn>] [-EmailAddresses <ProxyAddressCollection>]
 [-EmailAddressPolicyEnabled <$true | $false>] [-ExtensionCustomAttribute1 <MultiValuedProperty>]
 [-ExtensionCustomAttribute2 <MultiValuedProperty>] [-ExtensionCustomAttribute3 <MultiValuedProperty>]
 [-ExtensionCustomAttribute4 <MultiValuedProperty>] [-ExtensionCustomAttribute5 <MultiValuedProperty>]
 [-ForwardingAddress <RecipientIdParameter>] [-GrantSendOnBehalfTo <MultiValuedProperty>]
 [-HiddenFromAddressListsEnabled <$true | $false>] [-IgnoreDefaultScope] [-MailTip <String>]
 [-MailTipTranslations <MultiValuedProperty>] [-MaxReceiveSize <Unlimited>] [-MaxSendSize <Unlimited>]
 [-ModeratedBy <MultiValuedProperty>] [-ModerationEnabled <$true | $false>] [-Name <String>]
 [-PhoneticDisplayName <String>] [-PrimarySmtpAddress <SmtpAddress>]
 [-PublicFolderType <GeneralPurpose | Mapi | Nntp | NotSpecified>] [-RejectMessagesFrom <MultiValuedProperty>]
 [-RejectMessagesFromDLMembers <MultiValuedProperty>]
 [-RejectMessagesFromSendersOrMembers <MultiValuedProperty>]
 [-RequireSenderAuthenticationEnabled <$true | $false>]
 [-SendModerationNotifications <Never | Internal | Always>] [-Server <ServerIdParameter>]
 [-SimpleDisplayName <String>] [-UMDtmfMap <MultiValuedProperty>] [-WhatIf]
 [-WindowsEmailAddress <SmtpAddress>] [-EntryId <String>] [-ExternalEmailAddress <ProxyAddress>]
 [-ExternalDirectoryObjectId <Guid>] [-IgnoreMissingFolderLink <$true | $false>] [-OnPremisesObjectId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Recipients Provisioning Permissions" section in the Mailbox Permissions topic.

!!! Exchange Server 2013

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Public folders, mail-enabled" section in the Sharing and collaboration permissions topic.

!!! Exchange Server 2016, Exchange Online

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Set-MailPublicFolder -Identity MyPublicFolder@contoso.com -PrimarySmtpAddress MyPublicFolder@fabrikam.com
```

This example sets the primary SMTP address of the mail-enabled public folder MyPublicFolder@contoso.com to MyPublicFolder@fabrikam.com.

### Example 1 -------------------------- (Exchange Server 2013)
```
Set-MailPublicFolder -Identity MyPublicFolder@contoso.com -PrimarySmtpAddress MyPublicFolder@fabrikam.com
```

This example sets the primary SMTP address of the mail-enabled public folder MyPublicFolder@contoso.com to MyPublicFolder@fabrikam.com.

### Example 1 -------------------------- (Exchange Server 2016)
```
Set-MailPublicFolder -Identity MyPublicFolder@contoso.com -PrimarySmtpAddress MyPublicFolder@fabrikam.com
```

This example sets the primary SMTP address of the mail-enabled public folder MyPublicFolder@contoso.com to MyPublicFolder@fabrikam.com.

### Example 1 -------------------------- (Exchange Online)
```
Set-MailPublicFolder -Identity MyPublicFolder@contoso.com -PrimarySmtpAddress MyPublicFolder@fabrikam.com
```

This example sets the primary SMTP address of the mail-enabled public folder MyPublicFolder@contoso.com to MyPublicFolder@fabrikam.com.

## PARAMETERS

### -Identity
The Identity parameter specifies the GUID or public folder name that represents a specific public folder. You can also include the path using the format \\TopLevelPublicFolder\\PublicFolder.

You can omit the parameter label so that only the public folder name or GUID is supplied.

```yaml
Type: MailPublicFolderIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -AcceptMessagesOnlyFrom
!!! Exchange Server 2010

The AcceptMessagesOnlyFrom parameter specifies the mailbox users, mail users, and mail contacts that can send e-mail messages to this mail-enabled public folder. You can also specify Microsoft Exchange as a valid recipient for this parameter. If you configure a mail-enabled public folder to accept messages only from the Microsoft Exchange recipient, it only receives system-generated messages.

The AcceptMessagesOnlyFrom parameter can take any of the following values for valid senders:

- Distinguished name (DN)

- Canonical name

- GUID

- Name

- Display name

- Alias

- Exchange DN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The AcceptMessagesOnlyFrom parameter specifies the mailbox users, mail users, and mail contacts that can send email messages to this mail-enabled public folder. You can also specify Microsoft Exchange as a valid recipient for this parameter. If you configure a mail-enabled public folder to accept messages only from the Microsoft Exchange recipient, it only receives system-generated messages.

The AcceptMessagesOnlyFrom parameter can take any of the following values for valid senders:

- Distinguished name (DN)

- Canonical name

- GUID

- Name

- Display name

- Alias

- Exchange DN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The AcceptMessagesOnlyFrom parameter specifies who is allowed to send messages to this recipient. Messages from other senders are rejected.

Valid values for this parameter are individual senders in your organization (mailboxes, mail users, and mail contacts). You can use any value that uniquely identifies the sender. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple senders separated by commas. To overwrite any existing entries, use the following syntax: \<sender1\>,\<sender2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<sender1\>","\<sender2\>"....

To add or remove senders without affecting other existing entries, use the following syntax: @{Add="\<sender1\>","\<sender2\>"...; Remove="\<sender1\>","\<sender2\>"...}.

The senders you specify for this parameter are automatically copied to the AcceptMessagesOnlyFromSendersOrMembers property. Therefore, you can't use the AcceptMessagesOnlyFrom and AcceptMessagesOnlyFromSendersOrMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all senders.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AcceptMessagesOnlyFromDLMembers
!!! Exchange Server 2010

The AcceptMessagesOnlyFromDLMembers parameter specifies the distribution groups whose members are allowed to send e-mail messages to this mail-enabled public folder. You can use any of the following values for the allowed distribution groups:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The AcceptMessagesOnlyFromDLMembers parameter specifies the distribution groups whose members are allowed to send email messages to this mail-enabled public folder. You can use any of the following values for the allowed distribution groups:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The AcceptMessagesOnlyFromDLMembers parameter specifies who is allowed to send messages to this recipient. Messages from other senders are rejected.

Valid values for this parameter are groups in your organization (distribution groups, mail-enabled security groups, and dynamic distribution groups). Specifying a group means all members of the group are allowed to send messages to this recipient. You can use any value that uniquely identifies the group. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple groups separated by commas. To overwrite any existing entries, use the following syntax: \<group1\>,\<group2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<group1\>","\<group2\>"....

To add or remove groups without affecting other existing entries, use the following syntax: @{Add="\<group1\>","\<group2\>"...; Remove="\<group1\>","\<group2\>"...}.

The groups you specify for this parameter are automatically copied to the AcceptMessagesOnlyFromSendersOrMembers property. Therefore, you can't use the AcceptMessagesOnlyFromDLMembers and AcceptMessagesOnlyFromSendersOrMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all groups.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AcceptMessagesOnlyFromSendersOrMembers
!!! Exchange Server 2010

The AcceptMessagesOnlyFromSendersOrMembers parameter specifies the mailbox users, mail users, mail contacts, and distribution groups who are allowed to send e-mail messages to this mail-enabled public folder. You can use any of the following values for the allowed distribution groups:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The AcceptMessagesOnlyFromSendersOrMembers parameter specifies the mailbox users, mail users, mail contacts, and distribution groups who are allowed to send email messages to this mail-enabled public folder. You can use any of the following values for the allowed distribution groups:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The AcceptMessagesOnlyFromSendersOrMembers parameter specifies who is allowed to send messages to this recipient. Messages from other senders are rejected.

Valid values for this parameter are individual senders and groups in your organization. Individual senders are mailboxes, mail users, and mail contacts. Groups are distribution groups, mail-enabled security groups, and dynamic distribution groups. Specifying a group means all members of the group are allowed to send messages to this recipient.

To specify senders for this parameter, you can use any value that uniquely identifies the sender. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple senders separated by commas. To overwrite any existing entries, use the following syntax: \<sender1\>,\<sender2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<sender1\>","\<sender2\>"....

To add or remove individual senders or groups without affecting other existing entries, use the AcceptMessagesOnlyFrom and AcceptMessageOnlyFromDLMembers parameters.

The individual senders and groups you specify for this parameter are automatically copied to the AcceptMessagesOnlyFrom and AcceptMessagesOnlyFromDLMembers properties, respectively. Therefore, you can't use the AcceptMessagesOnlyFromSendersOrMembers parameter and the AcceptMessagesOnlyFrom or AcceptMessagesOnlyFromDLMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all senders.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Alias
!!! Exchange Server 2010, Exchange Server 2013

The Alias parameter specifies the alias (mail nickname) of the public folder. If not specified, the Alias parameter value is stamped with the name of the public folder.

The string must comply with RFC 2821 requirements for valid "local part" SMTP addresses.



!!! Exchange Server 2016, Exchange Online

The Alias parameter specifies the Exchange alias (also known as the mail nickname) for the recipient. This value identifies the recipient as a mail-enabled object, and shouldn't be confused with multiple email addresses for the same recipient (also known as proxy addresses). A recipient can have only one Alias value.

The value of Alias can contain letters, numbers and the characters !, #, $, %, &, ', \*, +, -, /, =, ?, ^, \_, `, {, |, } and ~. Periods (.) are allowed, but each period must be surrounded by other valid characters (for example, help.desk). Unicode characters from U+00A1 to U+00FF are also allowed. The maximum length of the Alias value is 64 characters.

When you create a recipient without specifying an email address, the Alias value you specify is used to generate the primary email address (\<alias\>@\<domain\>). Supported Unicode characters are mapped to best-fit US-ASCII text characters. For example, U+00F6 (ö) is changed to oe in the primary email address.

If you don't use the Alias parameter when you create a recipient, the value of a different required parameter is used for the Alias property value:

- Recipients with user accounts (for example, user mailboxes, and mail users): The left side of the MicrosoftOnlineServicesID or UserPrincipalName parameter is used. For example, helpdesk@contoso.com results in the Alias property value helpdesk.

- Recipeints without user accounts (for example, room mailboxes, mail contacts, and distribution groups): The value of the Name parameter is used. Spaces are removed and unsupported characters are converted to question marks (?).

If you modify the Alias value of an existing recipient, the primary email address is automatically updated only in on-premises environments where the recipient is subject to email address policies (the EmailAddressPolicyEnabled property is True for the recipient).

The Alias parameter never generates or updates the primary email address of a mail contact or a mail user.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArbitrationMailbox
The ArbitrationMailbox parameter specifies the mailbox used to manage the moderation process.

```yaml
Type: MailboxIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassModerationFromSendersOrMembers
!!! Exchange Server 2010

The BypassModerationFromSendersOrMembers parameter specifies the recipients whose messages bypass moderation when sending to this mail-enabled public folder. You can use any of the following values:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.

Senders designated as moderators for this mail-enabled public folder are allowed to send messages to this mail-enabled public folder.



!!! Exchange Server 2013

The BypassModerationFromSendersOrMembers parameter specifies the recipients whose messages bypass moderation when sending to this mail-enabled public folder. You can use any of the following values:

- DN

- Canonical name

- GUID

- Name

- Display name

- Legacy Exchange DN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.

Senders designated as moderators for this mail-enabled public folder are allowed to send messages to this mail-enabled public folder.



!!! Exchange Server 2016, Exchange Online

The BypassModerationFromSendersOrMembers parameter specifies who is allowed to send messages to this moderated recipient without approval from a moderator. Valid values for this parameter are individual senders and groups in your organization. Specifying a group means all members of the group are allowed to send messages to this recipient without approval from a moderator.

To specify senders for this parameter, you can use any value that uniquely identifies the sender. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

To enter multiple senders and overwrite any existing entries, use the following syntax: \<sender1\>,\<sender2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<sender1\>","\<sender2\>"....

To add or remove one or more senders without affecting any existing entries, use the following syntax: @{Add="\<sender1\>","\<sender2\>"...; Remove="\<sender3\>","\<sender4\>"...}.

This parameter is meaningful only when moderation is enabled for the recipient. By default, this parameter is blank ($null), which means messages from all senders other than the designated moderators are moderated. When a moderator sends a message to this recipient, the message is isn't moderated. In other words, you don't need to use this parameter to include the moderators.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contacts
!!! Exchange Server 2010

The Contacts parameter specifies the contacts for the public folder. Contacts are persons about whom you can save several types of information, such as addresses, telephone numbers, and Web page URLs.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The Contacts parameter specifies the contacts for the public folder. Contacts are persons about whom you can save several types of information, such as addresses, telephone numbers, and web page URLs.



```yaml
Type: RecipientIdParameter[]
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateDTMFMap
The CreateDTMFMap parameter specifies that a dual tone multi-frequency (DTMF) map be created for the user.

```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute1
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute10
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute11
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute12
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute13
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute14
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute15
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute2
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute3
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute4
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute5
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute6
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute7
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute8
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomAttribute9
The CustomAttribute1 to CustomAttribute15 parameters specify custom attributes. You can use these attributes to store additional information.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliverToMailboxAndForward
!!! Exchange Server 2010

The DeliverToMailboxAndForward parameter specifies whether e-mail messages are sent to a forwarding address.



!!! Exchange Server 2013

The DeliverToMailboxAndForward parameter specifies whether email messages are sent to a forwarding address.



!!! Exchange Server 2016, Exchange Online

The DeliverToMailboxAndForward parameter specifies the message delivery behavior when a forwarding address is specified by the ForwardingAddress or ForwardingSmtpAddress parameters. Valid values are:

- $true: Messages are delivered to this public folder and forwarded to the specified recipient or email address.

- $false: If a forwarding recipient or email address is configured, messages are delivered only to the specified recipient or email address, and messages aren't delivered to this public folder. If no forwarding recipient or email address is configured, messages are delivered only to this public folder.

The default value is $false. The value of this parameter is meaningful only if you configure a forwarding recipient or email address.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
!!! Exchange Server 2010

The DisplayName parameter specifies the display name of the Public Folder Proxy object



!!! Exchange Server 2013

The DisplayName parameter specifies the display name of the Public Folder Proxy object.



!!! Exchange Server 2016, Exchange Online

The DisplayName parameter specifies the display name of the Public Folder Proxy object.. The display name is visible in the Exchange admin center, address lists, and Outlook. The maximum length is 256 characters. If the value contains spaces, enclose the value in quotation marks (").



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
!!! Exchange Server 2010

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddresses
!!! Exchange Server 2010, Exchange Server 2013

The EmailAddresses parameter specifies proxy addresses (for example, user@contoso.com).



!!! Exchange Server 2016, Exchange Online

The EmailAddresses parameter specifies all the email addresses (proxy addresses) for the recipient, including the primary SMTP address. In on-premises Exchange organizations, the primary SMTP address and other proxy addresses are typically set by email address policies. However, you can use this parameter to configure other proxy addresses for the recipient. For more information, see Email address policies in Exchange 2016 (https://technet.microsoft.com/library/bb232171.aspx).

Valid syntax for this parameter is \<Type\>:\<emailaddress1\>,\<Type\>:\<emailaddress2\>.... The optional \<Type\> value specifies the type of email address. Some examples of valid values include:

- SMTP: The primary SMTP address. You can use this value only once in a command.

- smtp: Other SMTP email addresses.

- X400: X.400 addresses in on-premises Exchange.

- X500: X.500 addresses in on-premises Exchange.

If you don't include a \<Type\> value for an email address, the value smtp is assumed. Note that Exchange doesn't validate the syntax of custom address types (including X.400 addresses). Therefore, you need to verify that any custom addresses are formatted correctly.

To specify the primary SMTP email address, you can use any of the following methods:

- Use the \<Type\> value SMTP on the address.

- The first email address when you don't use any \<Type\> values, or when you use multiple \<Type\> values of smtp.

- If it's available, use the PrimarySmtpAddress parameter instead. You can't use the EmailAddresses parameter and the PrimarySmtpAddress parameter in the same command.

To replace all existing proxy email addresses with the values you specify, use the following syntax: "\<Type\>:\<emailaddress1\>","\<Type\>:\<emailaddress2\>"....

To add or remove specify proxy addresses without affecting other existing values, use the following syntax: @{Add="\<Type\>:\<emailaddress1\>","\<Type\>:\<emailaddress2\>"...; Remove="\<Type\>:\<emailaddress2\>","\<Type\>:\<emailaddress2\>"...}.



```yaml
Type: ProxyAddressCollection
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddressPolicyEnabled
!!! Exchange Server 2010

The EmailAddressPolicyEnabled parameter specifies whether to enable an e-mail address policy that's applied to the folder.



!!! Exchange Server 2013

The EmailAddressPolicyEnabled parameter specifies whether to enable an email address policy that's applied to the folder.



!!! Exchange Server 2016, Exchange Online

The EmailAddressPolicyEnabled parameter specifies whether to apply email address policies to this recipient. Valid values are:

- $true: Email address policies are applied to this recipient. This is the default value.

- $false: Email address policies aren't applied to this recipient.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionCustomAttribute1
!!! Exchange Server 2010

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Understanding Custom Attributes.

For more information about using multivalued properties, see Modifying Multivalued Properties.



!!! Exchange Server 2013

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes.

For more information about using multivalued properties, see Modifying multivalued properties.



!!! Exchange Server 2016, Exchange Online

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes (https://technet.microsoft.com/library/ee423541.aspx).

For more information about using multivalued properties, see Modifying multivalued properties (https://technet.microsoft.com/library/bb684908.aspx).



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionCustomAttribute2
!!! Exchange Server 2010

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Understanding Custom Attributes.

For more information about using multivalued properties, see Modifying Multivalued Properties.



!!! Exchange Server 2013

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes.

For more information about using multivalued properties, see Modifying multivalued properties.



!!! Exchange Server 2016, Exchange Online

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes (https://technet.microsoft.com/library/ee423541.aspx).

For more information about using multivalued properties, see Modifying multivalued properties (https://technet.microsoft.com/library/bb684908.aspx).



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionCustomAttribute3
!!! Exchange Server 2010

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Understanding Custom Attributes.

For more information about using multivalued properties, see Modifying Multivalued Properties.



!!! Exchange Server 2013

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes.

For more information about using multivalued properties, see Modifying multivalued properties.



!!! Exchange Server 2016, Exchange Online

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes (https://technet.microsoft.com/library/ee423541.aspx).

For more information about using multivalued properties, see Modifying multivalued properties (https://technet.microsoft.com/library/bb684908.aspx).



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionCustomAttribute4
!!! Exchange Server 2010

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Understanding Custom Attributes.

For more information about using multivalued properties, see Modifying Multivalued Properties.



!!! Exchange Server 2013

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes.

For more information about using multivalued properties, see Modifying multivalued properties.



!!! Exchange Server 2016, Exchange Online

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes (https://technet.microsoft.com/library/ee423541.aspx).

For more information about using multivalued properties, see Modifying multivalued properties (https://technet.microsoft.com/library/bb684908.aspx).



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionCustomAttribute5
!!! Exchange Server 2010

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Understanding Custom Attributes.

For more information about using multivalued properties, see Modifying Multivalued Properties.



!!! Exchange Server 2013

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes.

For more information about using multivalued properties, see Modifying multivalued properties.



!!! Exchange Server 2016, Exchange Online

The ExtensionCustomAttribute1-5 parameters specify custom attributes that store additional information. You can specify multiple values for these parameters as a comma delimited list. Each ExtensionCustomAttribute parameter can hold up to 1,300 values.

For more information about custom attributes, see Custom attributes (https://technet.microsoft.com/library/ee423541.aspx).

For more information about using multivalued properties, see Modifying multivalued properties (https://technet.microsoft.com/library/bb684908.aspx).



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForwardingAddress
!!! Exchange Server 2010, Exchange Server 2013

The ForwardingAddress parameter specifies the forwarding address of the folder.



!!! Exchange Server 2016, Exchange Online

The ForwardingAddress parameter specifies a forwarding address for messages that are sent to this public folder. A valid value for this parameter is a recipient in your organization. You can use any value that uniquely identifies the recipient.

For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

How messages are delivered and forwarded is controlled by the DeliverToMailboxAndForward parameter.

- DeliverToMailboxAndForward is $true: Messages are delivered to this public folder and forwarded to the specified recipient.

- DeliverToMailboxAndForward is $false: Messages are only forwarded to the specified recipient. Messages aren't delivered to this public folder.

The default value is blank ($null), which means no forwarding recipient is configured.



```yaml
Type: RecipientIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GrantSendOnBehalfTo
!!! Exchange Server 2010, Exchange Server 2013

The GrantSendOnBehalfTo parameter specifies the DN of other mailboxes that can send on behalf of this folder.



!!! Exchange Server 2016, Exchange Online

The GrantSendOnBehalfTo parameter specifies who can send on behalf of this public folder. Although messages sent on behalf of the mail user clearly show the sender in the From field (\<Sender\> on behalf of \<Public folder\>), replies to these messages are delivered to the public folder, not the sender.

The sender you specify for this parameter must a mailbox, mail user or mail-enabled security group (a mail-enabled security principal that can have permissions assigned). You can use any value that uniquely identifies the sender.

For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- \<domain name\>\\\<account name\>

- Email address

- GUID

- LegacyExchangeDN

- SamAccountName

- User ID or user principal name (UPN)

To enter multiple values and overwrite any existing entries, use the following syntax: \<value1\>,\<value2\>.... If the values contain spaces or otherwise require quotation marks, you need to use the following syntax: "\<value1\>","\<value2\>"....

To add or remove one or more values without affecting any existing entries, use the following syntax: @{Add="\<value1\>","\<value2\>"...; Remove="\<value1\>","\<value2\>"...}.

By default, this parameter is blank, which means no one else has permission to send on behalf of this public folder.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HiddenFromAddressListsEnabled
!!! Exchange Server 2010, Exchange Server 2013

The HiddenFromAddressListsEnabled parameter specifies whether the mailbox is viewable from address lists.



!!! Exchange Server 2016, Exchange Online

The HiddenFromAddressListsEnabled parameter specifies whether this recipient is visible in address lists. Valid values are:

- $true: The recipient isn't visible in address lists.

- $false: The recipient is visible in address lists. This is the default value.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreDefaultScope
!!! Exchange Server 2010, Exchange Server 2013

The IgnoreDefaultScope parameter instructs the command to ignore the default recipient scope setting for the Exchange Management Shell session and use the entire forest as the scope. This allows the command to access Active Directory objects that aren't currently in the default scope. Using the IgnoreDefaultScope parameter introduces the following restrictions:

- You can't use the DomainController parameter. The command uses an appropriate global catalog server automatically.



!!! Exchange Server 2016, Exchange Online

The IgnoreDefaultScope switch tells the command to ignore the default recipient scope setting for the Exchange Management Shell session, and to use the entire forest as the scope. This allows the command to access Active Directory objects that aren't currently available in the default scope.

Using the IgnoreDefaultScope switch introduces the following restrictions:

- You can't use the DomainController parameter. The command uses an appropriate global catalog server automatically.

- You can only use the DN for the Identity parameter. Other forms of identification, such as alias or GUID, aren't accepted.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailTip
!!! Exchange Server 2010

The MailTip parameter specifies the message that's displayed to senders when they start drafting an e-mail message to this recipient. The MailTip message must be less than or equal to 250 characters.



!!! Exchange Server 2013

The MailTip parameter specifies the message that's displayed to senders when they start drafting an email message to this recipient. The MailTip parameter message must be less than or equal to 250 characters.



!!! Exchange Server 2016, Exchange Online

The MailTip parameter specifies the custom MailTip text for this recipient. The MailTip is shown to senders when they start drafting an email message to this recipient. If the value contains spaces, enclose the value in quotation marks (").

When you add a MailTip to a recipient, two things happen:

- HTML tags are automatically added to the text. For example, if you enter the text: "This mailbox is not monitored", the MailTip automatically becomes: \<html\>\<body\>This mailbox is not monitored\</body\>\</html\>. Additional HTML tags aren't supported, and the length of the MailTip can't exceed 175 displayed characters.

- The text is automatically added to the MailTipTranslations property of the recipient as the default value: default:\<MailTip text\>. If you modify the MailTip text, the default value is automatically updated in the MailTipTranslations property, and vice-versa.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailTipTranslations
!!! Exchange Server 2010, Exchange Server 2013

The MailTipTranslations parameter specifies additional languages when you want to provide the MailTip parameter information for this recipient in multiple languages. For each language, you must provide the locale, followed by a colon and the specific MailTip parameter value in that language. Each MailTip parameter value must be less than or equal to 250 characters. Multiple languages can be separated by commas.



!!! Exchange Server 2016, Exchange Online

The MailTipTranslations parameter specifies additional languages for the custom MailTip text that's defined by the MailTip parameter. HTML tags are automatically added to the MailTip translation, additional HTML tags aren't supported, and the length of the MailTip translation can't exceed 175 displayed characters.

To add or remove MailTip translations without affecting the default MailTip or other MailTip translations, use the following syntax:

@{Add="\<culture 1\>:\<localized text 1\>","\<culture 2\>:\<localized text 2\>"...; Remove="\<culture 3\>:\<localized text 3\>","\<culture 4\>:\<localized text 4\>"...}

\<culture\> is a valid ISO 639 two-letter culture code that's associated with the language.

For example, suppose this recipient currently has the MailTip text: "This mailbox is not monitored." To add the Spanish translation, use the following value for this parameter: @{Add="ES:Esta caja no se supervisa."}.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxReceiveSize
!!! Exchange Server 2010

The MaxReceiveSize parameter specifies the maximum size of e-mail messages that can be received by the folder. Valid values are from 1 kilobyte (KB) to 2,097,151 KB. If a value isn't specified for this parameter, no size limit is imposed.



!!! Exchange Server 2013

The MaxReceiveSize parameter specifies the maximum size of email messages that can be received by the folder. Valid values are from 1 kilobyte (KB) to 2,097,151 KB. If a value isn't specified for this parameter, no size limit is imposed.



!!! Exchange Server 2016, Exchange Online

The MaxReceiveSize parameter specifies the maximum size of a message that can be sent to the public folder. Messages larger than the maximum size are rejected.

When you enter a value, qualify the value with one of the following units:

- B (bytes)

- KB (kilobytes)

- MB (megabytes)

- GB (gigabytes)

- TB (terabytes)

Unqualified values are typically treated as bytes, but small values may be rounded up to the nearest kilobyte.

A valid value is a number up to 1.999999 gigabytes (2147483647 bytes) or the value unlimited. The default value is unlimited.

The value unlimited indicates the maximum receive size for the public folder is controlled elsewhere (for example, organization, server, or connector limits).

For any message size limit, you need to set a value that's larger than the actual size you want enforced. This accounts for the Base64 encoding of attachments and other binary data. Base64 encoding increases the size of the message by approximately 33%, so the value you specify should be approximately 33% larger than the actual message size you want enforced. For example, if you specify a maximum message size value of 64 MB, you can expect a realistic maximum message size of approximately 48 MB.



```yaml
Type: Unlimited
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSendSize
!!! Exchange Server 2010

The MaxSendSize parameter specifies the maximum size of e-mail messages that can be sent. Valid values are from 1 KB to 2,097,151 KB. If a value isn't specified for this parameter, no size limit is imposed.



!!! Exchange Server 2013

The MaxSendSize parameter specifies the maximum size of email messages that can be sent. Valid values are from 1 KB to 2,097,151 KB. If a value isn't specified for this parameter, no size limit is imposed.



!!! Exchange Server 2016, Exchange Online

The MaxSendSize parameter specifies the maximum size of a message that can be sent by the public folder.

When you enter a value, qualify the value with one of the following units:

- B (bytes)

- KB (kilobytes)

- MB (megabytes)

- GB (gigabytes)

- TB (terabytes)

Unqualified values are typically treated as bytes, but small values may be rounded up to the nearest kilobyte.

A valid value is a number up to 1.999999 gigabytes (2147483647 bytes) or the value unlimited. The default value is unlimited.

The value unlimited indicates the maximum send size for the public folder is controlled elsewhere (for example, organization, server, or connector limits).

For any message size limit, you need to set a value that's larger than the actual size you want enforced. This accounts for the Base64 encoding of attachments and other binary data. Base64 encoding increases the size of the message by approximately 33%, so the value you specify should be approximately 33% larger than the actual message size you want enforced. For example, if you specify a maximum message size value of 64 MB, you can expect a realistic maximum message size of approximately 48 MB.



```yaml
Type: Unlimited
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModeratedBy
!!! Exchange Server 2010, Exchange Server 2013

The ModeratedBy parameter specifies the users who are responsible for moderating the messages sent to the mail-enabled public folder. To designate more than one user, separate the users with commas.

This parameter is required if you set the ModerationEnabled parameter to $true. If you leave this parameter blank and there is a user who is already specified as the manager of this distribution group, the ModeratedBy parameter is automatically set by the ManagedBy parameter of the mail-enabled public folder. Otherwise, an error is returned.



!!! Exchange Server 2016, Exchange Online

The ModeratedBy parameter specifies one or more moderators for this recipient. A moderator approves messages sent to the recipient before the messages are delivered. A moderator must be a mailbox, mail user, or mail contact in your organization. You can use any value that uniquely identifies the moderator.

For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

To enter multiple values and overwrite any existing entries, use the following syntax: \<value1\>,\<value2\>.... If the values contain spaces or otherwise require quotation marks, you need to use the following syntax: "\<value1\>","\<value2\>"....

To add or remove one or more values without affecting any existing entries, use the following syntax: @{Add="\<value1\>","\<value2\>"...; Remove="\<value1\>","\<value2\>"...}.

You need to use this parameter to specify at least one moderator when you set the ModerationEnabled parameter to the value $true.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModerationEnabled
!!! Exchange Server 2010, Exchange Server 2013

The ModerationEnabled parameter specifies whether to enable moderation for the mail-enabled public folder. To enable moderation, set this parameter to $true. To disable moderation, set this parameter to $false.

The default value is $false.



!!! Exchange Server 2016, Exchange Online

The ModerationEnabled parameter specifies whether moderation is enabled for this recipient. Valid value are:

- $true: Moderation is enabled for this recipient. Messages sent to this recipient must be approved by a moderator before the messages are delivered.

- $false: Moderation is disabled for this recipient. Messages sent to this recipient are delivered without the approval of a moderator. This is the default value.

You use the ModeratedBy parameter to specify the moderators.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
!!! Exchange Server 2010, Exchange Server 2013

The Name parameter specifies the name of the public folder. Use this parameter if you want to change the name of the public folder.



!!! Exchange Server 2016, Exchange Online

The Name parameter specifies the unique name of the public folder. The maximum length is 64 characters. If the value contains spaces, enclose the value in quotation marks (").



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhoneticDisplayName
!!! Exchange Server 2010

The PhoneticDisplayName parameter specifies a phonetic pronunciation of the DisplayName parameter.

The maximum length of this parameter value is 255 characters. For more information about the PhoneticDisplayName parameter and speech recognition, see Understanding Automatic Speech Recognition Directory Lookups.



!!! Exchange Server 2013

The PhoneticDisplayName parameter specifies a phonetic pronunciation of the DisplayName parameter.

The maximum length of this parameter value is 255 characters.



!!! Exchange Server 2016, Exchange Online

The PhoneticDisplayName parameter specifies an alternate spelling of the user's name that's used for text to speech in Unified Messaging (UM) environments. Typically, you use this parameter when the pronunciation and spelling of the user's name don't match. The maximum length is 256 characters. If the value contains spaces, enclose the value in quotation marks (").



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimarySmtpAddress
!!! Exchange Server 2010, Exchange Server 2013

The PrimarySmtpAddress parameter specifies the primary SMTP address for the folder.



!!! Exchange Server 2016, Exchange Online

The PrimarySmtpAddress parameter specifies the primary return email address that's used for the recipient. If it's available on this cmdlet, you can't use the EmailAddresses and PrimarySmtpAddress parameters in the same command.



```yaml
Type: SmtpAddress
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicFolderType
The PublicFolderType parameter specifies which of the following four types is assigned to the public folder:

- GeneralPurpose

- Mapi

- Nntp

- NotSpecified

```yaml
Type: GeneralPurpose | Mapi | Nntp | NotSpecified
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RejectMessagesFrom
!!! Exchange Server 2010

The RejectMessagesFrom parameter specifies the recipients from which to reject messages. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The RejectMessagesFrom parameter specifies the recipients from which to reject messages. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The RejectMessagesFrom parameter specifies who isn't allowed to send messages to this recipient. Messages from these senders are rejected.

Valid values for this parameter are individual senders in your organization (mailboxes, mail users, and mail contacts). You can use any value that uniquely identifies the sender. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple senders separated by commas. To overwrite any existing entries, use the following syntax: \<sender1\>,\<sender2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<sender1\>","\<sender2\>"....

To add or remove senders without affecting other existing entries, use the following syntax: @{Add="\<sender1\>","\<sender2\>"...; Remove="\<sender1\>","\<sender2\>"...}.

The senders you specify for this parameter are automatically copied to the RejectMessagesFromSendersOrMembers property. Therefore, you can't use the RejectMessagesFrom and RejectMessagesFromSendersOrMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all senders.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RejectMessagesFromDLMembers
!!! Exchange Server 2010

The RejectMessagesFromDLMembers parameter specifies the distribution list members from which to reject messages. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The RejectMessagesFromDLMembers parameter specifies the distribution list members from which to reject messages. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The RejectMessagesFromDLMembers parameter specifies who isn't allowed to send messages to this recipient. Messages from these senders are rejected.

Valid values for this parameter are groups in your organization (distribution groups, mail-enabled security groups, and dynamic distribution groups). Specifying a group means all members of the group aren't allowed to send messages to this recipient. You can use any value that uniquely identifies the group. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple groups separated by commas. To overwrite any existing entries, use the following syntax: \<group1\>,\<group2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<group1\>","\<group2\>"....

To add or remove groups without affecting other existing entries, use the following syntax: @{Add="\<group1\>","\<group2\>"...; Remove="\<group1\>","\<group2\>"...}.

The groups you specify for this parameter are automatically copied to the RejectMessagesFromSendersOrMembers property. Therefore, you can't use the RejectMessagesFromDLMembers and RejectMessagesFromSendersOrMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all groups.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RejectMessagesFromSendersOrMembers
!!! Exchange Server 2010

The RejectMessagesFromSendersOrMembers parameter specifies the mailbox users, mail users, mail contacts, and distribution groups whose members aren't allowed to send e-mail messages to this mail-enabled public folder. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP e-mail address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2013

The RejectMessagesFromSendersOrMembers parameter specifies the mailbox users, mail users, mail contacts, and distribution groups whose members aren't allowed to send email messages to this mail-enabled public folder. You can use any of the following values to specify the recipients:

- DN

- Canonical name

- GUID

- Name

- Display name

- LegacyExchangeDN

- Primary SMTP email address

By default, this parameter is blank. This default value enables the mail-enabled public folder to accept messages from all senders.



!!! Exchange Server 2016, Exchange Online

The RejectMessagesFromSendersOrMembers parameter specifies who isn't allowed to send messages to this recipient. Messages from these senders are rejected.

Valid values for this parameter are individual senders and groups in your organization. Individual senders are mailboxes, mail users, and mail contacts. Groups are distribution groups, mail-enabled security groups, and dynamic distribution groups. Specifying a group means all members of the group aren't allowed to send messages to this recipient.

To specify senders for this parameter, you can use any value that uniquely identifies the sender. For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- Email address

- GUID

You can enter multiple senders separated by commas. To overwrite any existing entries, use the following syntax: \<sender1\>,\<sender2\>.... If the values contain spaces or otherwise require quotation marks, use the following syntax: "\<sender1\>","\<sender2\>"....

To add or remove individual senders or groups without affecting other existing entries, use the RejectMessagesFrom and RejectMessagesFromDLMembers parameters.

The individual senders and groups you specify for this parameter are automatically copied to the RejectMessagesFrom and RejectMessagesFromDLMembers properties, respectively. Therefore, you can't use the RejectMessagesFromSendersOrMembers parameter and the RejectMessagesFrom or RejectMessagesFromDLMembers parameters in the same command.

By default, this parameter is blank ($null), which allows this recipient to accept messages from all senders.



```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireSenderAuthenticationEnabled
!!! Exchange Server 2010, Exchange Server 2013

The RequireSenderAuthenticationEnabled parameter specifies whether senders must be authenticated.



!!! Exchange Server 2016, Exchange Online

The RequireSenderAuthenticationEnabled parameter specifies whether to accept messages only from authenticated (internal) senders. Valid values are:

- $true: Messages are accepted only from authenticated (internal) senders. Messages from unauthenticated (external) senders are rejected.

- $false: Messages are accepted from authenticated (internal) and unauthenticated (external) senders.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendModerationNotifications
!!! Exchange Server 2010, Exchange Server 2013

The SendModerationNotifications parameter specifies whether status notifications are sent to users when they send a message to the moderated distribution group. You can specify one of the following values:

- Always

- Internal

- Never

Set this parameter to Always if you want notifications to be sent to all senders.

Set this parameter to Internal if you want notifications to be sent only to the senders who are internal to your organization.

Set this parameter to Never to disable all status notifications.

The sender is always notified if the message is rejected by the moderators, regardless of the value of this parameter.

The default value is Never.



!!! Exchange Server 2016, Exchange Online

The SendModerationNotifications parameter specifies when moderation notification messages are sent. Valid values are:

- Always: Notify all senders when their messages aren't approved. This is the default value.

- Internal: Notify senders in the organization when their messages aren't approved.

- Never: Don't notify anyone when a message isn't approved.

This parameter is only meaningful when moderation is enabled (the ModerationEnabled parameter has the value $true).



```yaml
Type: Never | Internal | Always
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
The Server parameter specifies the identity of the server to perform the operation from. If a server isn't specified, the command checks if the local server is a Mailbox server that is running Microsoft Exchange Server 2010 with a public folder database. If it is, the folder is created locally. If it isn't, the command finds the closest (by site cost) Exchange 2010 Mailbox server that has a mounted public folder database.

```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -SimpleDisplayName
The SimpleDisplayName parameter is used to display an alternative description of the object when only a limited set of characters is permitted. Valid characters are:

- a - z

- A - Z

- 0 - 9

- "\<space\>", """, "'", "(", ")", "+", ",", "-", ".", "/", ":", and "?".

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UMDtmfMap
The UMDtmfMap parameter specifies if you want to create a user-defined DTMF map for the UM-enabled user.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsEmailAddress
!!! Exchange Server 2010

The WindowsEmailAddress parameter specifies an e-mail address in the format E-mailAddress@contoso.com.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The WindowsEmailAddress parameter specifies an email address in the format EmailAddress@contoso.com.



```yaml
Type: SmtpAddress
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EntryId
The EntryId parameter specifies the EntryID value for the public folder. You use this parameter to correct an existing EntryID that points to a folder that can't be found.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalEmailAddress
The ExternalEmailAddress parameter specifies an email address outside the organization.

```yaml
Type: ProxyAddress
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalDirectoryObjectId
This parameter is reserved for internal Microsoft use.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreMissingFolderLink
The IgnoreMissingFolderLink parameter specifies whether to exclude the mail-enabled public folder from a specific validation check that's used during a public folder migration. Valid values are:

- $true: Skip the validation check. If the Active Directory object for the mail-enabled public folder doesn't have EntryId or ContentMailbox property values, the public folder is ignored, and the public folder migration can continue.

- $false: Don't skip the validation check. If the Active Directory object for the mail-enabled public folder doesn't have EntryId or ContentMailbox property values, the entire public folder migration will fail. This is the default value.

```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnPremisesObjectId
The OnPremisesObjectId parameter specifies the ObjectID (GUID) value of the mail-enabled public folder from the on-premises environment.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/8db48034-24cd-43d8-9133-1c8226616be5.aspx)
