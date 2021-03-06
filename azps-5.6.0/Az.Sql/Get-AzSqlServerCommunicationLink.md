---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 20f0fe00486b6b81ec1600e518c42121f5369095
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982075"
---
# Get-AzSqlServerCommunicationLink

## SYNOPSIS
데이터베이스 서버 간의 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 얻습니다.

## 구문

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Get-AzSqlServerCommunicationLink** cmdlet은 Azure SQL 데이터베이스에서 탄력적 데이터베이스 트랜잭션에 대한 서버 간 통신 링크를 제공합니다.
서버 통신 링크의 이름을 지정하여 해당 링크의 속성을 표시합니다.

## 예제

### 예제 1: 서버에 대한 모든 통신 링크 다운로드
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

이 명령은 ContosoServer17이라는 서버에 대한 탄력적 데이터베이스 트랜잭션에 대한 모든 서버 간 통신 링크를 얻습니다.

### 예제 2: 서버에 대한 특정 통신 링크 다운로드
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

이 명령은 Link01이라는 서버 간 통신 링크를 얻습니다.

### 예제 3: 필터링을 사용하여 서버에 대한 모든 통신 링크 다운로드
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

이 명령은 "Link"로 시작하는 ContosoServer17이라는 서버에 대한 탄력적 데이터베이스 트랜잭션에 대한 모든 서버 간 통신 링크를 얻습니다.

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

### -LinkName
이 cmdlet이 얻을 서버 통신 링크의 이름을 지정합니다.

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
*ServerName* 매개 변수에 의해 지정된 서버가 속하는 리소스 그룹의 이름을 지정합니다.

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

### -ServerName
서버 이름을 지정합니다.
이 서버에는 이 cmdlet이 도착하는 통신 링크가 포함되어 있습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql

## 관련 링크

[New-AzSqlServerCommunicationLink](./New-AzSqlServerCommunicationLink.md)

[Remove-AzSqlServerCommunicationLink](./Remove-AzSqlServerCommunicationLink.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
