---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034462"
---
# <span data-ttu-id="c7f30-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f30-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c7f30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f30-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f30-103">리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="c7f30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7f30-104">SYNTAX</span></span>

### <span data-ttu-id="c7f30-105">GetByResourceGroupDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7f30-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f30-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c7f30-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f30-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c7f30-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f30-108">**AzResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="c7f30-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c7f30-110">기본적으로 **Get-AzResourceGroupDeployment** 는 지정 된 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="c7f30-111">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="c7f30-112">Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="c7f30-113">배포는 리소스 그룹의 리소스를 사용할 수 있도록 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="c7f30-114">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f30-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c7f30-115">추적에이 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="c7f30-116">디버깅을 위해 Get-AzLog cmdlet에이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="c7f30-117">예제의</span><span class="sxs-lookup"><span data-stu-id="c7f30-117">EXAMPLES</span></span>

### <span data-ttu-id="c7f30-118">예제 1: 리소스 그룹에 대 한 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="c7f30-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="c7f30-119">이 명령은 ContosoLabsRG 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="c7f30-120">출력에는 갤러리 서식 파일을 사용 하는 WordPress 블로그의 배포가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="c7f30-121">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="c7f30-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="c7f30-122">이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="c7f30-123">**새 AzResourceGroup** 또는 **AzResourceGroupDeployment** cmdlet을 사용 하 여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="c7f30-124">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="c7f30-125">예제 3: 모든 리소스 그룹 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="c7f30-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="c7f30-126">이 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 구독에 있는 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c7f30-127">이 명령은 파이프라인 연산자를 사용 하 여 리소스 그룹을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c7f30-128">현재 cmdlet은 구독에 있는 모든 리소스 그룹의 모든 배포를 가져오고, 결과를 Format-Table cmdlet에 전달 하 여 **ResourceGroupName** , **Deploymentname** 및 **ProvisioningState** 속성 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="c7f30-129">변수</span><span class="sxs-lookup"><span data-stu-id="c7f30-129">PARAMETERS</span></span>

### <span data-ttu-id="c7f30-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c7f30-130">-ApiVersion</span></span>
<span data-ttu-id="c7f30-131">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c7f30-132">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c7f30-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f30-133">-DefaultProfile</span></span>
<span data-ttu-id="c7f30-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c7f30-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7f30-135">-Id</span><span class="sxs-lookup"><span data-stu-id="c7f30-135">-Id</span></span>
<span data-ttu-id="c7f30-136">가져올 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f30-137">-이름</span><span class="sxs-lookup"><span data-stu-id="c7f30-137">-Name</span></span>
<span data-ttu-id="c7f30-138">가져올 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="c7f30-139">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f30-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="c7f30-140">-Pre</span></span>
<span data-ttu-id="c7f30-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c7f30-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f30-142">-ResourceGroupName</span></span>
<span data-ttu-id="c7f30-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c7f30-144">Cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="c7f30-145">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="c7f30-146">이 매개 변수는 필수 이며 각 명령에 하나의 리소스 그룹만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f30-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f30-147">CommonParameters</span></span>
<span data-ttu-id="c7f30-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f30-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f30-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f30-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f30-150">입력</span><span class="sxs-lookup"><span data-stu-id="c7f30-150">INPUTS</span></span>

### <span data-ttu-id="c7f30-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7f30-151">System.String</span></span>

## <span data-ttu-id="c7f30-152">출력</span><span class="sxs-lookup"><span data-stu-id="c7f30-152">OUTPUTS</span></span>

### <span data-ttu-id="c7f30-153">SdkModels PSResourceGroupDeployment (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c7f30-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="c7f30-154">상속자</span><span class="sxs-lookup"><span data-stu-id="c7f30-154">NOTES</span></span>

## <span data-ttu-id="c7f30-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7f30-155">RELATED LINKS</span></span>

[<span data-ttu-id="c7f30-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7f30-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="c7f30-157">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7f30-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="c7f30-158">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f30-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="c7f30-159">제거-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f30-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c7f30-160">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f30-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="c7f30-161">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f30-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

