---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874031"
---
# <span data-ttu-id="a05b7-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a05b7-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a05b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b7-103">인스턴스 장애 조치 (Failover) 그룹의 장애 조치를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="a05b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a05b7-104">SYNTAX</span></span>

### <span data-ttu-id="a05b7-105">SwitchIFGDefault (기본값)</span><span class="sxs-lookup"><span data-stu-id="a05b7-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a05b7-106">리소스 Id에서 인스턴스 장애 조치 (Failover) 그룹 전환</span><span class="sxs-lookup"><span data-stu-id="a05b7-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b7-107">AzureSqlInstanceFailoverGroupModel 인스턴스 정의에서 인스턴스 장애 조치 (Failover) 그룹 전환</span><span class="sxs-lookup"><span data-stu-id="a05b7-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05b7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a05b7-108">DESCRIPTION</span></span>
<span data-ttu-id="a05b7-109">이 명령은 지정 된 보조 지역으로 장애 조치 (Failover) 하 여 새 기본 영역으로 변경 하 여 인스턴스 장애 조치 그룹의 관리 되는 인스턴스의 역할을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="a05b7-110">기본 끝점에 연결 하는 모든 새 TDS 세션은 자동으로 새 기본 영역으로 다시 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="a05b7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a05b7-111">EXAMPLES</span></span>

### <span data-ttu-id="a05b7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a05b7-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="a05b7-113">장애 조치 (failover) 작업을 수행 하 여 인스턴스 장애 조치 (Failover) 그룹의 파이핑에서 데이터 손실을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="a05b7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a05b7-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="a05b7-115">데이터 손실 또는 실패 및 롤백 없이 성공할 수 있는 최상의 장애 조치 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="a05b7-116">변수</span><span class="sxs-lookup"><span data-stu-id="a05b7-116">PARAMETERS</span></span>

### <span data-ttu-id="a05b7-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="a05b7-117">-AllowDataLoss</span></span>
<span data-ttu-id="a05b7-118">장애 조치를 완료 하면 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="a05b7-119">이렇게 하면 기본 데이터베이스를 사용할 수 없는 경우에도 장애 조치를 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b7-120">-DefaultProfile</span></span>
<span data-ttu-id="a05b7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a05b7-122">-InputObject</span></span>
<span data-ttu-id="a05b7-123">전환할 인스턴스 장애 조치 (Failover) 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="a05b7-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-124">-위치</span><span class="sxs-lookup"><span data-stu-id="a05b7-124">-Location</span></span>
<span data-ttu-id="a05b7-125">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="a05b7-126">-Name</span></span>
<span data-ttu-id="a05b7-127">인스턴스 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="a05b7-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a05b7-130">-ResourceId</span></span>
<span data-ttu-id="a05b7-131">전환할 인스턴스 장애 조치 (Failover) 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a05b7-132">-Confirm</span></span>
<span data-ttu-id="a05b7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05b7-134">-WhatIf</span></span>
<span data-ttu-id="a05b7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05b7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b7-137">CommonParameters</span></span>
<span data-ttu-id="a05b7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b7-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a05b7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b7-140">입력</span><span class="sxs-lookup"><span data-stu-id="a05b7-140">INPUTS</span></span>

### <span data-ttu-id="a05b7-141">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="a05b7-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="a05b7-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a05b7-142">System.String</span></span>

## <span data-ttu-id="a05b7-143">출력</span><span class="sxs-lookup"><span data-stu-id="a05b7-143">OUTPUTS</span></span>

### <span data-ttu-id="a05b7-144">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="a05b7-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a05b7-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a05b7-145">NOTES</span></span>

## <span data-ttu-id="a05b7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a05b7-146">RELATED LINKS</span></span>