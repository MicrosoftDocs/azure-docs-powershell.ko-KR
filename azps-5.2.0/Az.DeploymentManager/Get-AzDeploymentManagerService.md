---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324253"
---
# <span data-ttu-id="845ef-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="845ef-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="845ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="845ef-102">SYNOPSIS</span></span>
<span data-ttu-id="845ef-103">서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-103">Gets the service.</span></span>

## <span data-ttu-id="845ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="845ef-104">SYNTAX</span></span>

### <span data-ttu-id="845ef-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="845ef-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="845ef-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="845ef-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="845ef-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="845ef-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="845ef-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="845ef-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="845ef-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="845ef-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="845ef-110">설명</span><span class="sxs-lookup"><span data-stu-id="845ef-110">DESCRIPTION</span></span>
<span data-ttu-id="845ef-111">**Get-AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 반환하고 해당 서비스를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="845ef-112">해당 이름, 있는 서비스 토폴로지 및 리소스 그룹 이름으로 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="845ef-113">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="845ef-114">이 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerService cmdlet을 사용하여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="845ef-115">예제</span><span class="sxs-lookup"><span data-stu-id="845ef-115">EXAMPLES</span></span>

### <span data-ttu-id="845ef-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="845ef-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="845ef-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="845ef-118">예제 2: 리소스 식별자를 사용하여 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="845ef-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="845ef-120">예제 3: 서비스 개체를 사용하여 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="845ef-121">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 이름, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스를 $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="845ef-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="845ef-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="845ef-122">PARAMETERS</span></span>

### <span data-ttu-id="845ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845ef-123">-DefaultProfile</span></span>
<span data-ttu-id="845ef-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="845ef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="845ef-125">-InputObject</span></span>
<span data-ttu-id="845ef-126">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-127">-Name</span><span class="sxs-lookup"><span data-stu-id="845ef-127">-Name</span></span>
<span data-ttu-id="845ef-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="845ef-130">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="845ef-131">-ResourceId</span></span>
<span data-ttu-id="845ef-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="845ef-133">-ServiceTopologyName</span></span>
<span data-ttu-id="845ef-134">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-134">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="845ef-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="845ef-136">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="845ef-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="845ef-138">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845ef-139">CommonParameters</span></span>
<span data-ttu-id="845ef-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="845ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845ef-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="845ef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845ef-142">입력</span><span class="sxs-lookup"><span data-stu-id="845ef-142">INPUTS</span></span>

### <span data-ttu-id="845ef-143">System.String</span><span class="sxs-lookup"><span data-stu-id="845ef-143">System.String</span></span>

### <span data-ttu-id="845ef-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="845ef-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="845ef-145">출력</span><span class="sxs-lookup"><span data-stu-id="845ef-145">OUTPUTS</span></span>

### <span data-ttu-id="845ef-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="845ef-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="845ef-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="845ef-147">NOTES</span></span>

## <span data-ttu-id="845ef-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="845ef-148">RELATED LINKS</span></span>