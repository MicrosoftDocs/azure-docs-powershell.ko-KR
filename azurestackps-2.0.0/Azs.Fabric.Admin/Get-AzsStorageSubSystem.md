---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876062"
---
# Get-AzsStorageSubSystem

## SYNOPSIS
요청 된 저장소 하위 시스템을 반환 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### 가져오기
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## 설명은
요청 된 저장소 하위 시스템을 반환 합니다.

## 예제의

### 예제 1:
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

모든 저장소 하위 시스템을 배율 단위에서 가져옵니다.

### 예제 2:
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

확장 단위와 이름이 지정 된 저장소 하위 시스템을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -필터
OData 필터 매개 변수입니다.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -위치
리소스의 위치입니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -이름
저장소 시스템의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -PassThru
명령이 성공 하면 true를 반환 합니다.

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

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -ScaleUnit
눈금 단위의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -생략
OData skip 매개 변수입니다.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.
구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -위쪽
OData top 매개 변수.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell

## 출력

### FabricAdmin. Api20181001 Oragesubsystem을 지정 합니다.



## 상속자

복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.

INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수
  - `[Drive <String>]`: 저장소 드라이브의 이름입니다.
  - `[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.
  - `[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.
  - `[FabricLocation <String>]`: 패브릭 위치.
  - `[FileShare <String>]`: 패브릭 파일 공유 이름입니다.
  - `[IPPool <String>]`: IP 풀 이름입니다.
  - `[Id <String>]`: 리소스 id 경로
  - `[InfraRole <String>]`: 인프라 역할 이름입니다.
  - `[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.
  - `[Location <String>]`: 리소스의 위치입니다.
  - `[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.
  - `[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.
  - `[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.
  - `[Operation <String>]`: 작업 식별자입니다.
  - `[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.
  - `[ScaleUnit <String>]`: 눈금 단위 이름입니다.
  - `[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.
  - `[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.
  - `[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.
  - `[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.
  - `[Volume <String>]`: 저장소 볼륨의 이름입니다.

## 관련 링크

