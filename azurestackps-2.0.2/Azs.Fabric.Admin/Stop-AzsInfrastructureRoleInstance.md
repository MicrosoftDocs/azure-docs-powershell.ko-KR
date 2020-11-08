---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 07751ba4228faa578e4181ec481eef6e5b033126
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047124"
---
# <span data-ttu-id="49885-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="49885-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="49885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49885-102">SYNOPSIS</span></span>
<span data-ttu-id="49885-103">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="49885-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49885-104">SYNTAX</span></span>

### <span data-ttu-id="49885-105">PowerOff (기본값)</span><span class="sxs-lookup"><span data-stu-id="49885-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49885-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49885-106">PowerOffViaIdentity</span></span>
```
Stop-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49885-107">설명은</span><span class="sxs-lookup"><span data-stu-id="49885-107">DESCRIPTION</span></span>
<span data-ttu-id="49885-108">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="49885-109">예제의</span><span class="sxs-lookup"><span data-stu-id="49885-109">EXAMPLES</span></span>

### <span data-ttu-id="49885-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="49885-110">Example 1:</span></span> 
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="49885-111">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="49885-112">변수</span><span class="sxs-lookup"><span data-stu-id="49885-112">PARAMETERS</span></span>

### <span data-ttu-id="49885-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49885-113">-AsJob</span></span>
<span data-ttu-id="49885-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="49885-114">Run the command as a job</span></span>

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

### <span data-ttu-id="49885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49885-115">-DefaultProfile</span></span>
<span data-ttu-id="49885-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49885-117">-Force</span><span class="sxs-lookup"><span data-stu-id="49885-117">-Force</span></span>
<span data-ttu-id="49885-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49885-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="49885-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49885-119">-InputObject</span></span>
<span data-ttu-id="49885-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49885-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="49885-121">-위치</span><span class="sxs-lookup"><span data-stu-id="49885-121">-Location</span></span>
<span data-ttu-id="49885-122">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49885-123">-이름</span><span class="sxs-lookup"><span data-stu-id="49885-123">-Name</span></span>
<span data-ttu-id="49885-124">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49885-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="49885-125">-NoWait</span></span>
<span data-ttu-id="49885-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="49885-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="49885-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49885-127">-PassThru</span></span>
<span data-ttu-id="49885-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49885-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49885-129">-ResourceGroupName</span></span>
<span data-ttu-id="49885-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49885-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49885-131">-SubscriptionId</span></span>
<span data-ttu-id="49885-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49885-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-133">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49885-134">-확인</span><span class="sxs-lookup"><span data-stu-id="49885-134">-Confirm</span></span>
<span data-ttu-id="49885-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49885-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49885-136">-WhatIf</span></span>
<span data-ttu-id="49885-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49885-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49885-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49885-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49885-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49885-139">CommonParameters</span></span>
<span data-ttu-id="49885-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49885-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49885-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49885-142">입력</span><span class="sxs-lookup"><span data-stu-id="49885-142">INPUTS</span></span>

### <span data-ttu-id="49885-143">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="49885-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="49885-144">출력</span><span class="sxs-lookup"><span data-stu-id="49885-144">OUTPUTS</span></span>

### <span data-ttu-id="49885-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="49885-145">System.Boolean</span></span>



## <span data-ttu-id="49885-146">상속자</span><span class="sxs-lookup"><span data-stu-id="49885-146">NOTES</span></span>

<span data-ttu-id="49885-147">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49885-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="49885-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="49885-149">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="49885-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49885-150">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="49885-151">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="49885-152">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="49885-153">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="49885-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="49885-154">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="49885-155">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="49885-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="49885-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49885-157">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="49885-158">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="49885-159">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="49885-160">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="49885-161">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="49885-162">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="49885-163">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="49885-164">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="49885-165">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="49885-166">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="49885-167">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="49885-168">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="49885-169">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="49885-170">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="49885-171">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="49885-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="49885-172">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49885-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="49885-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49885-173">RELATED LINKS</span></span>
