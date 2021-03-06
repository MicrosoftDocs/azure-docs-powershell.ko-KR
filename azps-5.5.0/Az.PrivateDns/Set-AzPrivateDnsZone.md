---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179012"
---
# Set-AzPrivateDnsZone

## SYNOPSIS
리소스 그룹에서 사설 DNS 영역 업데이트

## 구문

### 필드(기본값)
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzPrivateDnsZone** cmdlet은 지정된 리소스 그룹에서 사설 DNS(도메인 이름 시스템) 영역이 영구적으로 업데이트됩니다.
*PrivateZone* 매개 변수를 사용하거나 파이프라인 연산자를 사용하여 **PrivateDnsZone** 개체를 전달하거나 *Name* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.
Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 업데이트되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로 계산, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다). 
이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.
이는 동시 변경  내용에 관계없이 영역이 업데이트되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.

## 예제

### 예제 1: 개인 영역 업데이트
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Name
이 cmdlet이 업데이트하는 개인 DNS 영역의 이름을 지정합니다.
*ResourceGroupName 매개 변수도 지정해야* 합니다.
또는 영역 매개 변수를 사용하여 사설 DNS 지역을 지정할 *수* 있습니다.

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

### -Overwrite
**PrivateDnsZone** 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **DnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 업데이트되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로 계산, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다).
이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.
이는 동시 변경  내용에 관계없이 영역이 업데이트되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.

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

### -PrivateZone
설정할 영역 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
업데이트할 영역이 포함된 리소스 그룹의 이름을 지정합니다.
*ZoneName 매개 변수도 지정해야* 합니다.
또는 파이프라인 또는 영역 매개 변수를 통해 전달된 **DnsZone** 개체를 사용하여 사설 DNS 지역을 지정할 *수* 있습니다.

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
사설 DNS 영역 ResourceID.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## 출력

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## 참고 사항

## 관련 링크

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
