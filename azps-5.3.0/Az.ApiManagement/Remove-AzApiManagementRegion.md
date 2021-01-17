---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381928"
---
# <span data-ttu-id="9abc1-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9abc1-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="9abc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9abc1-102">SYNOPSIS</span></span>
<span data-ttu-id="9abc1-103">PsApiManagement 인스턴스에서 기존 배포 지역을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="9abc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="9abc1-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9abc1-105">설명</span><span class="sxs-lookup"><span data-stu-id="9abc1-105">DESCRIPTION</span></span>
<span data-ttu-id="9abc1-106">**Remove-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement 형식의 인스턴스가 제공된 Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement의 추가Regions** 컬렉션에서 **Microsoft.Azure.Commands.ApiManagement** 유형의 인스턴스를 제거합니다. </span><span class="sxs-lookup"><span data-stu-id="9abc1-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9abc1-107">이 cmdlet은 자체적으로 배포를 수정하지 않지만 메모리 내 **PsApiManagement의** 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9abc1-108">API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagementInstance를** **Set-AzApiManagement에 전달합니다.**</span><span class="sxs-lookup"><span data-stu-id="9abc1-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="9abc1-109">예제</span><span class="sxs-lookup"><span data-stu-id="9abc1-109">EXAMPLES</span></span>

### <span data-ttu-id="9abc1-110">예제 1: PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="9abc1-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="9abc1-111">이 명령은 **PsApiManagement** 인스턴스에서 미국 동부라는 지역을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="9abc1-112">예제 2: 일련의 명령을 사용하여 PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="9abc1-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="9abc1-113">이 첫 번째 명령은 Contoso라는 Contoso라는 리소스 그룹에서 **PsApiManagement의** 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="9abc1-114">그런 다음, 마지막 명령은 해당 인스턴스에서 미국 동부라는 지역을 제거한 다음, 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="9abc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9abc1-115">PARAMETERS</span></span>

### <span data-ttu-id="9abc1-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9abc1-116">-ApiManagement</span></span>
<span data-ttu-id="9abc1-117">이 cmdlet이 추가 배포 지역을 제거하는 **PsApiManagement** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9abc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abc1-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="9abc1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9abc1-119">-Location</span></span>
<span data-ttu-id="9abc1-120">이 cmdlet이 제거하는 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="9abc1-121">Api Management 서비스에 대해 지원되는 지역 중에서 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="9abc1-122">유효한 위치를 얻습니다. -ProviderNamespace Get-AzResourceProvider "Microsoft.ApiManagement" cmdlet을 사용합니다. | where {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="9abc1-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abc1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abc1-123">CommonParameters</span></span>
<span data-ttu-id="9abc1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9abc1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abc1-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9abc1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abc1-126">입력</span><span class="sxs-lookup"><span data-stu-id="9abc1-126">INPUTS</span></span>

### <span data-ttu-id="9abc1-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9abc1-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="9abc1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9abc1-128">System.String</span></span>

## <span data-ttu-id="9abc1-129">출력</span><span class="sxs-lookup"><span data-stu-id="9abc1-129">OUTPUTS</span></span>

### <span data-ttu-id="9abc1-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9abc1-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9abc1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9abc1-131">NOTES</span></span>

## <span data-ttu-id="9abc1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9abc1-132">RELATED LINKS</span></span>

[<span data-ttu-id="9abc1-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9abc1-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="9abc1-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9abc1-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

