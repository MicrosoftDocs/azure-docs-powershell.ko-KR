---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: 707e7e4e702912d4d838913cb7ca030fef914e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197257"
---
# Get-AzVMwarePrivateCloud

## SYNOPSIS
사설 클라우드를 얻게

## 구문

### List1(기본값)
```
Get-AzVMwarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 목록
```
Get-AzVMwarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명
사설 클라우드를 얻게

## 예제

### 예제 1: 구독에 사설 클라우드 나열
```powershell
PS C:\> Get-AzVMwarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

구독에 사설 클라우드 나열

### 예제 2: 리소스 그룹 아래에 사설 클라우드 나열
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

리소스 그룹 아래에 사설 클라우드 나열

### 예제 3: 사설 클라우드 얻기
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

사설 클라우드를 얻게

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
사설 클라우드의 이름

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.
이름은 대소문자 무관합니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
대상 구독의 ID입니다.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IVMwareIdentity> ID 매개 변수
  - `[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름
  - `[ClusterName <String>]`: 사설 클라우드의 클러스터 이름
  - `[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름
  - `[Id <String>]`: 리소스 ID 경로
  - `[Location <String>]`: Azure 지역
  - `[PrivateCloudName <String>]`: 사설 클라우드의 이름
  - `[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다. 이름은 대소문자 무관합니다.
  - `[SubscriptionId <String>]`: 대상 구독의 ID입니다.

## 관련 링크

