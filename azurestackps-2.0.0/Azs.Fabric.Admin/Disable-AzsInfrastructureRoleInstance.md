---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876081"
---
# <span data-ttu-id="f1a9c-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f1a9c-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="f1a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a9c-102">SYNOPSIS</span></span>


## <span data-ttu-id="f1a9c-103">구문과</span><span class="sxs-lookup"><span data-stu-id="f1a9c-103">SYNTAX</span></span>

### <span data-ttu-id="f1a9c-104">시스템 종료 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1a9c-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1a9c-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1a9c-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1a9c-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f1a9c-106">DESCRIPTION</span></span>
<span data-ttu-id="f1a9c-107">유지 관리를 위해 인프라 역할 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="f1a9c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f1a9c-108">EXAMPLES</span></span>

### <span data-ttu-id="f1a9c-109">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f1a9c-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="f1a9c-110">유지 관리를 위해 인프라 역할 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="f1a9c-111">변수</span><span class="sxs-lookup"><span data-stu-id="f1a9c-111">PARAMETERS</span></span>

### <span data-ttu-id="f1a9c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a9c-112">-AsJob</span></span>
<span data-ttu-id="f1a9c-113">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f1a9c-113">Run the command as a job</span></span>

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

### <span data-ttu-id="f1a9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a9c-114">-DefaultProfile</span></span>
<span data-ttu-id="f1a9c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a9c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f1a9c-116">-Force</span></span>
<span data-ttu-id="f1a9c-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f1a9c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1a9c-118">-InputObject</span></span>
<span data-ttu-id="f1a9c-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-120">-위치</span><span class="sxs-lookup"><span data-stu-id="f1a9c-120">-Location</span></span>
<span data-ttu-id="f1a9c-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f1a9c-122">-Name</span></span>
<span data-ttu-id="f1a9c-123">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1a9c-124">-NoWait</span></span>
<span data-ttu-id="f1a9c-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f1a9c-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1a9c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1a9c-126">-PassThru</span></span>
<span data-ttu-id="f1a9c-127">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1a9c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a9c-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1a9c-129">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1a9c-130">-SubscriptionId</span></span>
<span data-ttu-id="f1a9c-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1a9c-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f1a9c-133">-Confirm</span></span>
<span data-ttu-id="f1a9c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a9c-135">-WhatIf</span></span>
<span data-ttu-id="f1a9c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a9c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1a9c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a9c-138">CommonParameters</span></span>
<span data-ttu-id="f1a9c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a9c-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a9c-141">입력</span><span class="sxs-lookup"><span data-stu-id="f1a9c-141">INPUTS</span></span>

### <span data-ttu-id="f1a9c-142">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="f1a9c-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f1a9c-143">출력</span><span class="sxs-lookup"><span data-stu-id="f1a9c-143">OUTPUTS</span></span>

### <span data-ttu-id="f1a9c-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f1a9c-144">System.Boolean</span></span>



## <span data-ttu-id="f1a9c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f1a9c-145">NOTES</span></span>

<span data-ttu-id="f1a9c-146">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1a9c-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f1a9c-148">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1a9c-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1a9c-149">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f1a9c-150">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f1a9c-151">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f1a9c-152">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f1a9c-153">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f1a9c-154">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f1a9c-155">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f1a9c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1a9c-156">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f1a9c-157">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f1a9c-158">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f1a9c-159">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f1a9c-160">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f1a9c-161">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f1a9c-162">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f1a9c-163">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f1a9c-164">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f1a9c-165">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f1a9c-166">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f1a9c-167">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f1a9c-168">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f1a9c-169">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f1a9c-170">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f1a9c-171">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f1a9c-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1a9c-172">RELATED LINKS</span></span>
