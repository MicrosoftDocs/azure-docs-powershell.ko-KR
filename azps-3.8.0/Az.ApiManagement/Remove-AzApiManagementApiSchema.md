---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045069"
---
# <span data-ttu-id="2aa31-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2aa31-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="2aa31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa31-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa31-103">Api에서 API 스키마를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="2aa31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2aa31-104">SYNTAX</span></span>

### <span data-ttu-id="2aa31-105">ByApiSchemaId (기본값)</span><span class="sxs-lookup"><span data-stu-id="2aa31-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa31-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2aa31-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa31-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa31-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa31-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2aa31-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa31-109">Api에서 cmdlet을 제거 하는 **AzApiManagementSchema** .</span><span class="sxs-lookup"><span data-stu-id="2aa31-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="2aa31-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2aa31-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa31-111">예제 1: API에서 Api 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="2aa31-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="2aa31-112">`2`참조 하지 않는 경우 스크립트는 Api에서 스키마를 제거 `echo-api` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="2aa31-113">변수</span><span class="sxs-lookup"><span data-stu-id="2aa31-113">PARAMETERS</span></span>

### <span data-ttu-id="2aa31-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2aa31-114">-ApiId</span></span>
<span data-ttu-id="2aa31-115">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-115">Identifier of the API.</span></span>
<span data-ttu-id="2aa31-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa31-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2aa31-117">-Context</span></span>
<span data-ttu-id="2aa31-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2aa31-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa31-120">-DefaultProfile</span></span>
<span data-ttu-id="2aa31-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa31-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa31-122">-InputObject</span></span>
<span data-ttu-id="2aa31-123">PsApiManagementApiSchema의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="2aa31-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa31-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa31-125">-PassThru</span></span>
<span data-ttu-id="2aa31-126">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2aa31-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="2aa31-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa31-128">-ResourceId</span></span>
<span data-ttu-id="2aa31-129">ApiSchema의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="2aa31-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa31-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="2aa31-131">-SchemaId</span></span>
<span data-ttu-id="2aa31-132">API 스키마의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="2aa31-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa31-134">-확인</span><span class="sxs-lookup"><span data-stu-id="2aa31-134">-Confirm</span></span>
<span data-ttu-id="2aa31-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa31-136">-WhatIf</span></span>
<span data-ttu-id="2aa31-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa31-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa31-139">CommonParameters</span></span>
<span data-ttu-id="2aa31-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa31-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2aa31-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa31-142">입력</span><span class="sxs-lookup"><span data-stu-id="2aa31-142">INPUTS</span></span>

### <span data-ttu-id="2aa31-143">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2aa31-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2aa31-144">ApiManagement. ServiceManagement. \ PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2aa31-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="2aa31-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2aa31-145">System.String</span></span>

## <span data-ttu-id="2aa31-146">출력</span><span class="sxs-lookup"><span data-stu-id="2aa31-146">OUTPUTS</span></span>

### <span data-ttu-id="2aa31-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2aa31-147">System.Boolean</span></span>

## <span data-ttu-id="2aa31-148">상속자</span><span class="sxs-lookup"><span data-stu-id="2aa31-148">NOTES</span></span>

## <span data-ttu-id="2aa31-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2aa31-149">RELATED LINKS</span></span>

[<span data-ttu-id="2aa31-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2aa31-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="2aa31-151">새로운 AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2aa31-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="2aa31-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2aa31-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)