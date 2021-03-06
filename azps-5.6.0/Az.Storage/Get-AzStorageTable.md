---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994793"
---
# Get-AzStorageTable

## SYNOPSIS
저장소 테이블을 나열합니다.

## 구문

### TableName(기본값)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzStorageTable** cmdlet에는 Azure의 저장소 계정과 연결된 저장소 테이블이 나열됩니다.

## 예제

### 예제 1: 모든 Azure Storage 테이블 나열
```
PS C:\>Get-AzStorageTable
```

이 명령은 Storage 계정에 대한 모든 저장소 테이블을 얻습니다.

### 예제 2: 와일드카드 문자를 사용하여 Azure Storage 테이블 나열
```
PS C:\>Get-AzStorageTable -Name table*
```

이 명령은 와일드카드 문자를 사용하여 이름이 테이블로 시작하는 저장소 테이블을 얻습니다.

### 예제 3: 테이블 이름 연결부를 사용하여 Azure Storage 테이블 나열
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

이 명령은 *Prefix* 매개 변수를 사용하여 이름이 테이블로 시작하는 저장소 테이블을 얻습니다.

## 매개 변수

### -Context
저장소 컨텍스트를 지정합니다.
만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
테이블 이름을 지정합니다.
테이블 이름이 비어 있는 경우 cmdlet에는 모든 테이블이 나열됩니다.
그렇지 않으면 지정된 이름 또는 일반 이름 패턴과 일치하는 모든 테이블이 나열됩니다.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
얻을 테이블 또는 테이블의 이름에 사용되는 도두를 지정합니다.
이 기능을 사용하여 테이블과 같은 문자열로 시작하는 모든 테이블을 찾을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## 참고 사항

## 관련 링크

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


