---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056612"
---
# <span data-ttu-id="db437-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="db437-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="db437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db437-102">SYNOPSIS</span></span>
<span data-ttu-id="db437-103">API 버전 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db437-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="db437-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db437-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db437-105">설명은</span><span class="sxs-lookup"><span data-stu-id="db437-105">DESCRIPTION</span></span>
<span data-ttu-id="db437-106">**AzApiManagementApiVersionSet** Cmdlet은 Azure api MANAGEMENT 컨텍스트에서 API 버전 집합 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db437-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="db437-107">예제의</span><span class="sxs-lookup"><span data-stu-id="db437-107">EXAMPLES</span></span>

### <span data-ttu-id="db437-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="db437-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="db437-109">이 명령은 버전 지정 체계 `Query` 와 쿼리 매개 변수를 설정 하는 API 버전 집합을 만듭니다 `api-version` .</span><span class="sxs-lookup"><span data-stu-id="db437-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="db437-110">변수</span><span class="sxs-lookup"><span data-stu-id="db437-110">PARAMETERS</span></span>

### <span data-ttu-id="db437-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="db437-111">-ApiVersionSetId</span></span>
<span data-ttu-id="db437-112">새 API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="db437-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-113">This parameter is optional.</span></span>
<span data-ttu-id="db437-114">지정 하지 않으면 식별자가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db437-114">If not specified an identifier will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="db437-115">-Context</span></span>
<span data-ttu-id="db437-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db437-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db437-118">-DefaultProfile</span></span>
<span data-ttu-id="db437-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db437-120">-설명</span><span class="sxs-lookup"><span data-stu-id="db437-120">-Description</span></span>
<span data-ttu-id="db437-121">Api 버전 집합에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-121">Description of the Api Version set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-122">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="db437-122">-HeaderName</span></span>
<span data-ttu-id="db437-123">버전 관리 정보가 포함 될 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="db437-124">버전 지정 체계 헤더가 선택 된 경우에는이 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db437-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-125">-이름</span><span class="sxs-lookup"><span data-stu-id="db437-125">-Name</span></span>
<span data-ttu-id="db437-126">ApiVersion Set의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="db437-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-127">This parameter is required.</span></span>

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

### <span data-ttu-id="db437-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="db437-128">-QueryName</span></span>
<span data-ttu-id="db437-129">버전 관리 정보를 포함할 쿼리 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="db437-130">버전 지정 체계 쿼리를 선택한 경우에는이 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db437-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-131">-구성표</span><span class="sxs-lookup"><span data-stu-id="db437-131">-Scheme</span></span>
<span data-ttu-id="db437-132">Api 버전 설정에 대해 선택할 버전 지정 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="db437-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db437-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db437-134">-확인</span><span class="sxs-lookup"><span data-stu-id="db437-134">-Confirm</span></span>
<span data-ttu-id="db437-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db437-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db437-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db437-136">-WhatIf</span></span>
<span data-ttu-id="db437-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db437-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db437-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db437-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db437-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db437-139">CommonParameters</span></span>
<span data-ttu-id="db437-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db437-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db437-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db437-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db437-142">입력</span><span class="sxs-lookup"><span data-stu-id="db437-142">INPUTS</span></span>

### <span data-ttu-id="db437-143">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db437-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db437-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db437-144">System.String</span></span>

### <span data-ttu-id="db437-145">ApiManagement. ServiceManagement. \ PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="db437-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="db437-146">출력</span><span class="sxs-lookup"><span data-stu-id="db437-146">OUTPUTS</span></span>

### <span data-ttu-id="db437-147">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="db437-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="db437-148">상속자</span><span class="sxs-lookup"><span data-stu-id="db437-148">NOTES</span></span>

## <span data-ttu-id="db437-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db437-149">RELATED LINKS</span></span>

[<span data-ttu-id="db437-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="db437-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="db437-151">제거-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="db437-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="db437-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="db437-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)