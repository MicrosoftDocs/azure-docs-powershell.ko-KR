---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381935"
---
# <span data-ttu-id="cffab-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cffab-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="cffab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cffab-102">SYNOPSIS</span></span>
<span data-ttu-id="cffab-103">기존 구독을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="cffab-104">구문</span><span class="sxs-lookup"><span data-stu-id="cffab-104">SYNTAX</span></span>

### <span data-ttu-id="cffab-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="cffab-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cffab-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cffab-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cffab-108">설명</span><span class="sxs-lookup"><span data-stu-id="cffab-108">DESCRIPTION</span></span>
<span data-ttu-id="cffab-109">**Remove-AzApiManagementSubscription** cmdlet은 기존 구독을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="cffab-110">예제</span><span class="sxs-lookup"><span data-stu-id="cffab-110">EXAMPLES</span></span>

### <span data-ttu-id="cffab-111">예제 1: 구독 삭제</span><span class="sxs-lookup"><span data-stu-id="cffab-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="cffab-112">이 명령은 기존 구독을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="cffab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cffab-113">PARAMETERS</span></span>

### <span data-ttu-id="cffab-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cffab-114">-Context</span></span>
<span data-ttu-id="cffab-115">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="cffab-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cffab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffab-116">-DefaultProfile</span></span>
<span data-ttu-id="cffab-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cffab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cffab-118">-InputObject</span></span>
<span data-ttu-id="cffab-119">PsApiManagementSubscription의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="cffab-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cffab-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cffab-121">-PassThru</span></span>
<span data-ttu-id="cffab-122">이 cmdlet이 성공하는 경우 $True 값 또는 $false 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="cffab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cffab-123">-ResourceId</span></span>
<span data-ttu-id="cffab-124">구독의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="cffab-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffab-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cffab-126">-SubscriptionId</span></span>
<span data-ttu-id="cffab-127">구독 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="cffab-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cffab-128">-Confirm</span></span>
<span data-ttu-id="cffab-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffab-130">-WhatIf</span></span>
<span data-ttu-id="cffab-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cffab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffab-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffab-133">CommonParameters</span></span>
<span data-ttu-id="cffab-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cffab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffab-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cffab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffab-136">입력</span><span class="sxs-lookup"><span data-stu-id="cffab-136">INPUTS</span></span>

### <span data-ttu-id="cffab-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cffab-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cffab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cffab-138">System.String</span></span>

### <span data-ttu-id="cffab-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cffab-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cffab-140">출력</span><span class="sxs-lookup"><span data-stu-id="cffab-140">OUTPUTS</span></span>

### <span data-ttu-id="cffab-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cffab-141">System.Boolean</span></span>

## <span data-ttu-id="cffab-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cffab-142">NOTES</span></span>

## <span data-ttu-id="cffab-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cffab-143">RELATED LINKS</span></span>

[<span data-ttu-id="cffab-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cffab-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="cffab-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cffab-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="cffab-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cffab-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)

