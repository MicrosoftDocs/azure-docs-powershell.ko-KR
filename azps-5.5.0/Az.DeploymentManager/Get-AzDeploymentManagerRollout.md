---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198017"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
롤아웃을 얻습니다.

## 구문

### 대화형(기본값)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzDeploymentManagerRollout** cmdlet은 롤아웃을 구하고 롤아웃 진행률에 대한 모든 세부 정보가 있는 해당 롤아웃을 나타내는 개체를 반환합니다.
이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다. 또는 Rollout 개체 또는 ResourceId를 제공할 수 있습니다.

반환된 롤아웃 개체에는 배포된 서비스, 서비스 단위 및 단계 및 진행 중 단계가 포함되어 있습니다. 아직 배포되지 않은 것은 응답에 없습니다.

## 예제

### 예제 1 롤아웃하기
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다. 

### 예제 2 롤아웃 세부 정보 표시
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다. -Verbose 스위치는 모든 롤아웃 세부 정보를 계층적으로 표시됩니다. 롤아웃의 전체적인 보기에 대한 각 단계에 대한 서비스, ServiceUnits 및 각 ServiceUnit의 단계 및 컨텍스트 정보를 보여 줄 수 있습니다.

### 예제 3: 리소스 식별자를 사용하여 롤아웃하기
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다.

### 예제 4: 롤아웃 개체를 사용하여 롤아웃합니다.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 롤아웃을 $rolloutObject.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
롤아웃 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
롤아웃의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
롤아웃의 재시도입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## 출력

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## 참고 사항

## 관련 링크
