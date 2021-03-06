---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883233"
---
# Get-AzureStorageQueue

## SYNOPSIS
저장소 큐를 나열 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### QueueName (기본값)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureStorageQueue** Cmdlet은 Azure 저장소 계정과 연결 된 저장소 큐를 나열 합니다.

## 예제의

### 예제 1: 모든 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue
```

이 명령은 현재 저장소 계정에 대 한 모든 저장소 큐의 목록을 가져옵니다.

### 예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

이 명령은 와일드 카드 문자를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.

### 예제 3: 큐 이름 접두사를 사용 하 여 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

이 예제에서는 *Prefix* 매개 변수를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
**새로운-AzureStorageContext** cmdlet을 사용 하 여 만들 수 있습니다.

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

### -이름
이름을 지정 합니다.
이름을 지정 하지 않으면 cmdlet에서 모든 큐의 목록을 가져옵니다.
전체 또는 일부 이름을 지정한 경우 cmdlet은 이름 패턴과 일치 하는 모든 큐를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -접두사
가져오려는 큐 이름에 사용 되는 접두사를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.

## 상속자

## 관련 링크

[새로운 AzureStorageQueue](./New-AzureStorageQueue.md)

[제거-AzureStorageQueue](./Remove-AzureStorageQueue.md)


