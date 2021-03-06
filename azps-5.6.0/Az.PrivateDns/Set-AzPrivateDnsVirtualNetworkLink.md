---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 1e1fa3709e597d220ba8269856f562a8ad8c3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985726"
---
# Set-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
개인 영역 및 리소스 그룹과 연결된 가상 네트워크 링크를 업데이트/설정합니다.

## 구문

### 필드(기본값)
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### 개체
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹의 영역과 연결된 링크를 업데이트합니다.
링크 매개 변수를 사용하여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름  *영역* 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. 
확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.
**PSPrivateDnsVirtualNetworkLink** 개체(파이프라인 또는 링크 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 변경된 경우 링크가 업데이트되지 않습니다. 그러면 동시 링크 변경에 대한 보호가 제공됩니다. 이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 링크를 업데이트합니다. 

## 예제

### 예제 1: 링크 설정
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

이 명령은 MyResourceGroup이라는 리소스 그룹에서 myzone.com 명명된 영역과 연결된 mylink라는 링크에 대해 IsRegistrationEnabled를 True로 설정합니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
설정할 가상 네트워크 링크 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsRegistrationEnabled
가상 네트워크 링크에서 등록이 활성화되어 있는 경우를 나타내는 부울입니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet이 제거한 링크의 이름을 지정합니다.
*ResourceGroupName* 및 *ZoneName 매개 변수도 지정해야* 합니다.
또는 링크 매개 변수를 사용하여 개인 DNS 링크를 지정할 *수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -덮어 덮어 덮어 덮어 덮어
**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 변경된 경우 링크가 삭제되지 않습니다.
그러면 동시 링크 변경에 대한 보호가 제공됩니다.
이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 링크를 삭제합니다. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
제거할 링크가 포함된 리소스 그룹의 이름을 지정합니다.
*ZoneName* 및 Name 매개 변수도 *지정해야* 합니다.
또는 파이프라인 또는 링크 매개 변수를 통해 전달된 **PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 가상 네트워크 링크를 지정할 *수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
개인 DNS 영역 ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
리소스 태그를 나타내는 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneName
이 cmdlet이 제거한 DNS 영역의 이름을 지정합니다.
이름 및 *ResourceGroupName 매개 변수도 지정해야* 합니다. 
또는 링크 매개 변수를 사용하여 개인 DNS 링크를 지정할 *수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink

### System.String

## 출력

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink

## 참고 사항

## 관련 링크

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
