---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: ee12c80843433200d6bf48818665156830cf2941
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529993"
---
# New-AzureRmSqlDatabaseFailoverGroup

## SYNOPSIS
이 명령은 새 Azure SQL 데이터베이스 장애 조치 그룹을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
지정 된 서버에 대 한 새 Azure SQL 데이터베이스 장애 조치 그룹을 만듭니다.

두 개의 Azure SQL Database TDS 끝점은 Failovergroupname (예: FailoverGroupName.database.windows.net) 및 FailoverGroupName. SqlDatabaseDnsSuffix에 만들어집니다. 이러한 끝점을 사용 하 여 장애 조치 그룹의 기본 및 보조 서버에 각각 연결할 수 있습니다. 주 서버가 작동 중지에 영향을 받는 경우, 끝점 및 데이터베이스의 자동 장애 조치는 장애 조치 그룹의 장애 조치 정책 및 유예 기간에 따라 트리거됩니다.

새로 만든 장애 조치 (Failover) 그룹에는 데이터베이스가 포함 되지 않습니다. 장애 조치 (Failover) 그룹의 데이터베이스 집합을 제어 하려면 ' AzureRmSqlDatabaseToFailoverGroup ' 및 ' Remove-AzureRmSqlDatabaseFromFailoverGroup ' cmdlet을 사용 합니다.

장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.

## 예제의

### 예제 1
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

이 명령은 같은 리소스 그룹의 두 서버에 대해 장애 조치 정책으로 새 장애 조치 (failover) 그룹을 만듭니다.

### 예제 2
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

이 명령은 서로 다른 리소스 그룹의 두 서버에 대해 장애 조치 정책 ' 수동 '을 사용 하 여 새 장애 조치 그룹을 만듭니다.

## 변수

### -AllowReadOnlyFailoverToPrimary
보조 서버의 작동 중지가 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부 이 기능은 아직 지원 되지 않습니다.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverGroupName
만들 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
Azure SQL Database 장애 조치 (Failover) 그룹의 장애 조치 정책

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
기본 서버에서 작동 중지가 발생 하 고 데이터 손실 없이 장애 조치를 완료할 수 없는 경우 자동 장애 조치가 시작 되기 전의 간격입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Azure SQL Database 장애 조치 (Failover) 그룹의 보조 리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -(-)-(서버 이름)
Azure SQL Database 장애 조치 (Failover) 그룹의 보조 서버 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

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
장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### System. 개체

## 상속자

## 관련 링크

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[Get-AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[추가-AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[제거-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[스위치-AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[제거-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
