---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b4484d06802a8b17fc08b359b5dafb7e0a406ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007531"
---
# New-AzStreamAnalyticsOutput

## SYNOPSIS
Stream Analytics 작업의 출력을 생성하거나 업데이트합니다.

## 구문

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzStreamAnalyticsOutput** cmdlet은 Stream Analytics 작업 내에서 출력을 생성하거나 기존 출력을 업데이트합니다.
출력의 이름은 에서 지정할 수 있습니다. JSON 파일 또는 명령줄에 있습니다.
둘 다 지정되어 있는 경우 명령줄의 이름은 파일의 이름과 일치해야 합니다.
이미 있는 출력을 지정하고 *Force* 매개 변수를 지정하지 않으면 cmdlet에서 기존 출력을 바꿀지 여부를 묻습니다.
Force 매개  변수를 지정하고 기존 출력 이름을 지정하면 출력이 확인 없이 대체됩니다.

## 예제

### 예제 1: 작업의 출력 추가
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

이 명령은 StreamingJob이라는 작업에서 Output이라는 새 출력을 만듭니다.
이 이름이 있는 기존 출력이 이미 정의되어 있는 경우 cmdlet에서 이 출력을 바꿀지 여부를 묻습니다.

### 예제 2: 작업 출력 정의 바꾸기
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

이 명령은 확인 없이 StreamingJob이라는 작업의 출력 정의를 대체합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -File
만들 Azure Stream Analytics 출력의 JSON 표현이 포함된 JSON 파일의 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Azure Stream Analytics 출력을 만들 Azure Stream Analytics 작업의 이름을 지정합니다.

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

### -Name
만들 Azure Stream Analytics 출력의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Stream Analytics 출력을 만들 리소스 그룹의 이름을 지정합니다.

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

### System.String

## 출력

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput

## 참고 사항

## 관련 링크

[Get-AzStreamAnalyticsOutput](./Get-AzStreamAnalyticsOutput.md)

[Remove-AzStreamAnalyticsOutput](./Remove-AzStreamAnalyticsOutput.md)

[Test-AzStreamAnalyticsOutput](./Test-AzStreamAnalyticsOutput.md)


