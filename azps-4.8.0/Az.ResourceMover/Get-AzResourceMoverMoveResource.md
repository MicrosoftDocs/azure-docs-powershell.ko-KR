---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204902"
---
# <span data-ttu-id="1f7ac-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="1f7ac-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="1f7ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7ac-103">이동 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="1f7ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f7ac-104">SYNTAX</span></span>

### <span data-ttu-id="1f7ac-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f7ac-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f7ac-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1f7ac-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f7ac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f7ac-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7ac-108">이동 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="1f7ac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f7ac-109">EXAMPLES</span></span>

### <span data-ttu-id="1f7ac-110">예제 1: 이동 컬렉션의 모든 리소스에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="1f7ac-111">이동 컬렉션의 모든 리소스에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="1f7ac-112">예제 2: 리소스 이름 이동을 사용 하 여 이동 컬렉션의 특정 리소스에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f7ac-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="1f7ac-113">리소스 이름 이동을 사용 하 여 이동 컬렉션의 특정 리소스에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="1f7ac-114">예제 3: SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState 등의 필터를 사용 하 여 이동 컬렉션의 특정 리소스에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="1f7ac-115">Armid, moveStatusMoveState (verify) 등의 필터를 사용 하 여 이동 컬렉션의 특정 리소스에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="1f7ac-116">변수</span><span class="sxs-lookup"><span data-stu-id="1f7ac-116">PARAMETERS</span></span>

### <span data-ttu-id="1f7ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7ac-117">-DefaultProfile</span></span>
<span data-ttu-id="1f7ac-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f7ac-119">-필터</span><span class="sxs-lookup"><span data-stu-id="1f7ac-119">-Filter</span></span>
<span data-ttu-id="1f7ac-120">작업에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="1f7ac-121">예를 들어 $filter = Properties/ProvisioningState eq ' Succeeded '를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

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

### <span data-ttu-id="1f7ac-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1f7ac-122">-MoveCollectionName</span></span>
<span data-ttu-id="1f7ac-123">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1f7ac-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1f7ac-124">-Name</span></span>
<span data-ttu-id="1f7ac-125">이동 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f7ac-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1f7ac-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f7ac-128">-SubscriptionId</span></span>
<span data-ttu-id="1f7ac-129">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7ac-130">CommonParameters</span></span>
<span data-ttu-id="1f7ac-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7ac-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7ac-133">입력</span><span class="sxs-lookup"><span data-stu-id="1f7ac-133">INPUTS</span></span>

## <span data-ttu-id="1f7ac-134">출력</span><span class="sxs-lookup"><span data-stu-id="1f7ac-134">OUTPUTS</span></span>

### <span data-ttu-id="1f7ac-135">Api20191001Preview. IMoveResource에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7ac-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="1f7ac-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1f7ac-136">NOTES</span></span>

<span data-ttu-id="1f7ac-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="1f7ac-137">ALIASES</span></span>

## <span data-ttu-id="1f7ac-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f7ac-138">RELATED LINKS</span></span>
