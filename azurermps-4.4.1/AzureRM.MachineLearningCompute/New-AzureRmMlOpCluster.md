---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533060"
---
# New-AzureRmMlOpCluster

## SYNOPSIS
새 operationalization 클러스터를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### OperationalizationCluster 인스턴스 정의에서 새 operationalization 클러스터를 만듭니다.
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### Cmdlet 입력 매개 변수를 통해 새 operationalization 클러스터를 만듭니다.
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## 설명은
새 operationalization 클러스터를 만듭니다. 이렇게 하면 클러스터 개체, 컨테이너 서비스, 필요한 경우, application insights, azure 컨테이너 레지스트리가 만들어집니다.

## 예제의

### 예제 1
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

Orchestrator로 azure 컨테이너 서비스와 Kubernetes를 사용 하 여 새 operationalization 클러스터를 만듭니다.

### 예제 2
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

로컬에서 새 operationalization 클러스터를 만듭니다. 이렇게 하면 azure 컨테이너 레지스트리, application insights 및 저장소 계정이 만들어지지만 컨테이너 서비스는 생성 되지 않습니다.

## 변수

### -AgentCount
ACS 클러스터의 에이전트 노드 수입니다.

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgentVmSize
ACS 클러스터의 에이전트 노드 수입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContainerRegistry
Azure 컨테이너 레지스트리에 대 한 URI로,이를 만드는 대신 사용할 수 있습니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Operationalization 클러스터 속성입니다.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
Operationalization 클러스터 유형입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -설명
ACS 클러스터의 마스터 노드 수입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationAdditionalProperties
전역 서비스 구성에 대 한 추가 속성입니다.

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationETag
업데이트에 대 한 구성 ETag입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
Operationalization 클러스터의 위치입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MasterCount
ACS 클러스터의 마스터 노드 수입니다.

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Operationalization 클러스터의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrchestratorType
ACS 클러스터의 orchestrator 유형입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId
ACS 클러스터의 orchestrator service principal id입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -비밀
ACS 클러스터의 orchestrator service principal secret.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCName
SSL 인증서에 대 한 CName

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
Base64 문자열로 인코딩된 PEM 형식의 SSL 인증서 데이터입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslKey
Base64 문자열로 인코딩된 PEM 형식의 SSL 키 데이터입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslStatus
SSL 상태
가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
저장소 계정 중 하나를 만드는 대신 사용 하는 URI입니다.

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### 않아야


## 출력

### MachineLearningCompute. PSOperationalizationCluster/.


## 상속자

## 관련 링크

