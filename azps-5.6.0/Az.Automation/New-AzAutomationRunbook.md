---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: 1f9d913ed250aa4c4a0dee2a72d5bd434b97e08c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010011"
---
# New-AzAutomationRunbook

## SYNOPSIS
Automation Runbook을 만듭니다.

## 구문

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzAutomationRunbook** cmdlet은 APS를 사용하여 빈 Azure Automation Runbook을 만듭니다.
Runbook의 이름을 지정합니다.

## 예제

### 예제 1: Runbook 만들기
```powershell
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

이 명령은 Contoso17이라는 Azure Automation 계정에 Runbook02라는 Runbook을 만듭니다.

### 예제 2

Automation Runbook을 만듭니다. (자동 재생)

<!-- Aladdin Generated Example -->


```powershell
New-AzAutomationRunbook -AutomationAccountName 'Contoso17' -Name 'Runbook02' -ResourceGroupName 'ResourceGroup01' -Type PowerShell
```

## 매개 변수

### -AutomationAccountName
이 cmdlet에서 Runbook을 만드는 Automation 계정의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Description
Runbook에 대한 설명을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogProgress
Runbook 로그가 진행률인지 여부를 지정합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogVerbose
로깅에 자세한 정보가 포함되어 있는지 여부를 지정합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Runbook의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet에서 Runbook을 만드는 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
해시 테이블의 형태로 키 값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
이 cmdlet에서 만드는 Runbook 유형을 지정합니다.
유효한 값은:
- PowerShell
- GraphicalPowerShell
- PowerShellWorkflow
- GraphicalPowerShellWorkflow
- 그래프
- Python2 값 그래프는 사용되지 않습니다.
GraphicalPowerShellWorkflow와 동일합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2, Python3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Collections.IDictionary

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Automation.Model.Runbook

## 참고 사항

## 관련 링크

[Export-AzAutomationRunbook](./Export-AzAutomationRunbook.md)

[Get-AzAutomationRunbook](./Get-AzAutomationRunbook.md)

[Import-AzAutomationRunbook](./Import-AzAutomationRunbook.md)

[Publish-AzAutomationRunbook](./Publish-AzAutomationRunbook.md)

[Remove-AzAutomationRunbook](./Remove-AzAutomationRunbook.md)

[Set-AzAutomationRunbook](./Set-AzAutomationRunbook.md)

[Start-AzAutomationRunbook](./Start-AzAutomationRunbook.md)
