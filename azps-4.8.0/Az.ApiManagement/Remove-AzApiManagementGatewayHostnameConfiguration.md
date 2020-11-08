---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048547"
---
# <span data-ttu-id="f88e5-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f88e5-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f88e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f88e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f88e5-103">기존 게이트웨이에서 호스트 이름 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="f88e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f88e5-104">SYNTAX</span></span>

### <span data-ttu-id="f88e5-105">ContextParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f88e5-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88e5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f88e5-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88e5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f88e5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f88e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f88e5-108">DESCRIPTION</span></span>
<span data-ttu-id="f88e5-109">**AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에서 호스트 이름 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="f88e5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f88e5-110">EXAMPLES</span></span>

### <span data-ttu-id="f88e5-111">예제 1: 기존 게이트웨이 호스트 이름 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f88e5-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="f88e5-112">이 명령은 기존 게이트웨이 호스트 이름 구성을 제거 하 고 사용자에 게 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="f88e5-113">변수</span><span class="sxs-lookup"><span data-stu-id="f88e5-113">PARAMETERS</span></span>

### <span data-ttu-id="f88e5-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f88e5-114">-Context</span></span>
<span data-ttu-id="f88e5-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f88e5-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="f88e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88e5-117">-DefaultProfile</span></span>
<span data-ttu-id="f88e5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88e5-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f88e5-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="f88e5-120">기존 게이트웨이 호스트 이름 구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="f88e5-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-121">This parameter is required.</span></span>

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

### <span data-ttu-id="f88e5-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f88e5-122">-GatewayId</span></span>
<span data-ttu-id="f88e5-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="f88e5-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f88e5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f88e5-125">-InputObject</span></span>
<span data-ttu-id="f88e5-126">PsApiManagementGatewayHostnameConfiguration의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="f88e5-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f88e5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f88e5-128">-PassThru</span></span>
<span data-ttu-id="f88e5-129">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f88e5-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-130">This parameter is optional.</span></span>
<span data-ttu-id="f88e5-131">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-131">Default value is false.</span></span>

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

### <span data-ttu-id="f88e5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f88e5-132">-ResourceId</span></span>
<span data-ttu-id="f88e5-133">GatewayHostnameConfiguration의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="f88e5-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-134">This parameter is required.</span></span>

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

### <span data-ttu-id="f88e5-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f88e5-135">-Confirm</span></span>
<span data-ttu-id="f88e5-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f88e5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f88e5-137">-WhatIf</span></span>
<span data-ttu-id="f88e5-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f88e5-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f88e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88e5-140">CommonParameters</span></span>
<span data-ttu-id="f88e5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88e5-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f88e5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88e5-143">입력</span><span class="sxs-lookup"><span data-stu-id="f88e5-143">INPUTS</span></span>

### <span data-ttu-id="f88e5-144">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f88e5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f88e5-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f88e5-145">System.String</span></span>

### <span data-ttu-id="f88e5-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f88e5-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f88e5-147">출력</span><span class="sxs-lookup"><span data-stu-id="f88e5-147">OUTPUTS</span></span>

### <span data-ttu-id="f88e5-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f88e5-148">System.Boolean</span></span>

## <span data-ttu-id="f88e5-149">상속자</span><span class="sxs-lookup"><span data-stu-id="f88e5-149">NOTES</span></span>

## <span data-ttu-id="f88e5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f88e5-150">RELATED LINKS</span></span>