---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213725"
---
# Get-AzAutomationDscNodeConfiguration

## SYNOPSIS
자동화에서 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfigurationName
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzAutomationDscNodeConfiguration** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성에 대 한 메타 데이터를 가져옵니다.
자동화는 DSC 노드 구성을 MOF (관리 개체 형식) 구성 문서로 저장 합니다.

## 예제의

### 예제 1: 모든 DSC 노드 구성 가져오기
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 Automation 계정의 모든 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.

### 예제 2: DSC 구성에 대 한 모든 DSC 노드 구성 가져오기
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

이 명령은 ContosoConfiguration 이라는 DSC 구성이 생성 Contoso17 이라는 자동화 계정의 모든 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.

### 예제 3: 이름별로 DSC 노드 구성 가져오기
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConfiguration 이름을 사용 하 여 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.

## 변수

### -AutomationAccountName
이 cmdlet이 메타 데이터를 가져오는 DSC 노드 구성을 포함 하는 자동화 계정의 이름을 지정 합니다.

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

### -ConfigurationName
이 cmdlet이 노드 구성 메타 데이터를 가져오는 DSC 구성의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -이름
이 cmdlet에서 메타 데이터를 가져오는 DSC 노드 구성의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.

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

### -RollupStatus
이 cmdlet이 가져오는 DSC 노드 구성의 롤업 상태를 지정 합니다.
유효한 값은 다음과 같습니다. 
- 잘못 
- 적합

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### CompilationJob를 통해 서.

## 상속자

## 관련 링크

[가져오기-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)


