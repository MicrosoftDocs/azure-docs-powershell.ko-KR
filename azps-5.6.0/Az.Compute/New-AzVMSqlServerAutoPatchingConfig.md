---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001739"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
가상 머신에서 자동 패치를 위한 구성 개체를 만듭니다.

## 구문

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## 설명
**New-AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 머신의 자동 패치를 위한 구성 개체를 만듭니다.

## 예제

### 예제 1: 자동 패치를 구성하는 구성 개체 만들기
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

이 명령은 패치를 위한 구성 개체를 만듭니다.
명령은 주일을 지정하고 유지 관리 기간을 정의합니다.
이 구성은 이러한 값을 사용하는 패치를 가능하게 합니다.
명령은 결과를 $AutoBackupConfig 저장합니다.
다른 cmdlet(예: cmdlet)에 대해 이 Set-AzVMSqlServerExtension 수 있습니다.

## 매개 변수

### -DayOfWeek
업데이트를 설치해야 하는 주일을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 일요일
- 월요일
- 화요일
- 수요일
- 목요일
- 금요일
- 토요일
- 매일

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용하도록 설정
가상 머신에 대한 자동화된 패치가 사용하도록 설정되어 있는 경우를 나타냅니다.
cmdlet을 자동화된 패치를 사용하도록 설정하면 Windows 업데이트를 대화형 모드로 전환합니다.
자동 패치를 사용하지 않도록 설정하면 Windows 업데이트 설정이 변경되지 않습니다.

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

### -MaintenanceWindowDuration
유지 관리 기간의 기간(분)을 지정합니다.
자동화된 패치는 이 창 외부의 가상 머신 가용성에 영향을 줄 수 있는 작업을 수행하지 않습니다.
30분의 배수를 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
유지 관리 기간이 시작되는 시간을 지정합니다.
이번에는 업데이트가 설치하기 시작하는 시기를 정의합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
중요한 업데이트를 포함해야 하는지 여부를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## 참고 사항

## 관련 링크

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


