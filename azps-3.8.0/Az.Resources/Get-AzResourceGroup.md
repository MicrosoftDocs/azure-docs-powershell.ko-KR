---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043916"
---
# <span data-ttu-id="8b509-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b509-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="8b509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b509-102">SYNOPSIS</span></span>
<span data-ttu-id="8b509-103">리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-103">Gets resource groups.</span></span>

## <span data-ttu-id="8b509-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b509-104">SYNTAX</span></span>

### <span data-ttu-id="8b509-105">GetByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b509-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b509-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8b509-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b509-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8b509-107">DESCRIPTION</span></span>
<span data-ttu-id="8b509-108">**AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="8b509-109">모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="8b509-110">기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="8b509-111">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b509-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="8b509-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8b509-112">EXAMPLES</span></span>

### <span data-ttu-id="8b509-113">예제 1: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b509-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="8b509-114">이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="8b509-115">예제 2: 리소스 그룹의 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b509-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="8b509-116">이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="8b509-117">예제 3: 위치를 기준으로 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="8b509-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="8b509-118">예제 4: 특정 위치에 있는 모든 리소스 그룹의 이름 표시</span><span class="sxs-lookup"><span data-stu-id="8b509-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="8b509-119">예제 5: 이름이 WebServer로 시작 하는 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="8b509-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="8b509-120">예제 6: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b509-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="8b509-121">이 명령은 "EngineerBlog"로 시작 하는 구독의 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="8b509-122">변수</span><span class="sxs-lookup"><span data-stu-id="8b509-122">PARAMETERS</span></span>

### <span data-ttu-id="8b509-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b509-123">-ApiVersion</span></span>
<span data-ttu-id="8b509-124">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8b509-125">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8b509-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b509-126">-DefaultProfile</span></span>
<span data-ttu-id="8b509-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8b509-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b509-128">-Id</span><span class="sxs-lookup"><span data-stu-id="8b509-128">-Id</span></span>
<span data-ttu-id="8b509-129">가져올 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="8b509-130">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b509-131">-위치</span><span class="sxs-lookup"><span data-stu-id="8b509-131">-Location</span></span>
<span data-ttu-id="8b509-132">가져올 리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-132">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b509-133">-이름</span><span class="sxs-lookup"><span data-stu-id="8b509-133">-Name</span></span>
<span data-ttu-id="8b509-134">가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="8b509-135">이 매개 변수는 문자열의 시작 및/또는 끝에 있는 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8b509-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b509-136">-Pre</span></span>
<span data-ttu-id="8b509-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b509-138">태그</span><span class="sxs-lookup"><span data-stu-id="8b509-138">-Tag</span></span>
<span data-ttu-id="8b509-139">리소스 그룹을 필터링 하는 태그 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-139">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b509-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b509-140">CommonParameters</span></span>
<span data-ttu-id="8b509-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b509-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b509-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b509-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b509-143">입력</span><span class="sxs-lookup"><span data-stu-id="8b509-143">INPUTS</span></span>

### <span data-ttu-id="8b509-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8b509-144">System.String</span></span>

### <span data-ttu-id="8b509-145">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8b509-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b509-146">출력</span><span class="sxs-lookup"><span data-stu-id="8b509-146">OUTPUTS</span></span>

### <span data-ttu-id="8b509-147">SdkModels PSResourceGroup. m a.</span><span class="sxs-lookup"><span data-stu-id="8b509-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="8b509-148">상속자</span><span class="sxs-lookup"><span data-stu-id="8b509-148">NOTES</span></span>

## <span data-ttu-id="8b509-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b509-149">RELATED LINKS</span></span>

[<span data-ttu-id="8b509-150">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b509-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8b509-151">제거-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b509-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="8b509-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b509-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

