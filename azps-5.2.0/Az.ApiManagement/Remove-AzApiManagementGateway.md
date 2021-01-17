---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361376"
---
# <span data-ttu-id="4877a-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4877a-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="4877a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4877a-102">SYNOPSIS</span></span>
<span data-ttu-id="4877a-103">게이트웨이에서 API를 디스어치합니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="4877a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4877a-104">SYNTAX</span></span>

### <span data-ttu-id="4877a-105">ContextParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4877a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4877a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4877a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4877a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4877a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4877a-108">설명</span><span class="sxs-lookup"><span data-stu-id="4877a-108">DESCRIPTION</span></span>
<span data-ttu-id="4877a-109">**Remove-AzApiManagementGateway** cmdlet은 게이트웨이에서 API를 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="4877a-110">예제</span><span class="sxs-lookup"><span data-stu-id="4877a-110">EXAMPLES</span></span>

### <span data-ttu-id="4877a-111">예제 1: 기존 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="4877a-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="4877a-112">이 명령은 기존 게이트웨이를 제거하고 사용자에게 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="4877a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4877a-113">PARAMETERS</span></span>

### <span data-ttu-id="4877a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4877a-114">-Context</span></span>
<span data-ttu-id="4877a-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4877a-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4877a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4877a-117">-DefaultProfile</span></span>
<span data-ttu-id="4877a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4877a-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="4877a-119">-GatewayId</span></span>
<span data-ttu-id="4877a-120">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="4877a-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4877a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4877a-122">-InputObject</span></span>
<span data-ttu-id="4877a-123">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="4877a-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4877a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4877a-125">-PassThru</span></span>
<span data-ttu-id="4877a-126">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4877a-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-127">This parameter is optional.</span></span>
<span data-ttu-id="4877a-128">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-128">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4877a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4877a-129">-ResourceId</span></span>
<span data-ttu-id="4877a-130">게이트웨이의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="4877a-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-131">This parameter is required.</span></span>

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

### <span data-ttu-id="4877a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4877a-132">-Confirm</span></span>
<span data-ttu-id="4877a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4877a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4877a-134">-WhatIf</span></span>
<span data-ttu-id="4877a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4877a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4877a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4877a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4877a-137">CommonParameters</span></span>
<span data-ttu-id="4877a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4877a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4877a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4877a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4877a-140">입력</span><span class="sxs-lookup"><span data-stu-id="4877a-140">INPUTS</span></span>

### <span data-ttu-id="4877a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4877a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4877a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4877a-142">System.String</span></span>

### <span data-ttu-id="4877a-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4877a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4877a-144">출력</span><span class="sxs-lookup"><span data-stu-id="4877a-144">OUTPUTS</span></span>

### <span data-ttu-id="4877a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4877a-145">System.Boolean</span></span>

## <span data-ttu-id="4877a-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4877a-146">NOTES</span></span>

## <span data-ttu-id="4877a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4877a-147">RELATED LINKS</span></span>