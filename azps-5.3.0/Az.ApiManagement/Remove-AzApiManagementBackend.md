---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382166"
---
# <span data-ttu-id="4df5e-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4df5e-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="4df5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df5e-102">SYNOPSIS</span></span>
<span data-ttu-id="4df5e-103">백end를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-103">Removes a Backend.</span></span>

## <span data-ttu-id="4df5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4df5e-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="4df5e-105">DESCRIPTION</span></span>
<span data-ttu-id="4df5e-106">API Management에서 식별자가 지정한 백레드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="4df5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="4df5e-107">EXAMPLES</span></span>

### <span data-ttu-id="4df5e-108">예제 1: 백end 123 제거</span><span class="sxs-lookup"><span data-stu-id="4df5e-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="4df5e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df5e-109">PARAMETERS</span></span>

### <span data-ttu-id="4df5e-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="4df5e-110">-BackendId</span></span>
<span data-ttu-id="4df5e-111">기존 백end의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-111">Identifier of existing backend.</span></span>
<span data-ttu-id="4df5e-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-112">This parameter is required.</span></span>

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

### <span data-ttu-id="4df5e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4df5e-113">-Context</span></span>
<span data-ttu-id="4df5e-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4df5e-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4df5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df5e-116">-DefaultProfile</span></span>
<span data-ttu-id="4df5e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df5e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df5e-118">-PassThru</span></span>
<span data-ttu-id="4df5e-119">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4df5e-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-120">This parameter is optional.</span></span>
<span data-ttu-id="4df5e-121">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-121">Default value is false.</span></span>

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

### <span data-ttu-id="4df5e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df5e-122">-Confirm</span></span>
<span data-ttu-id="4df5e-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df5e-124">-WhatIf</span></span>
<span data-ttu-id="4df5e-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4df5e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4df5e-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df5e-127">CommonParameters</span></span>
<span data-ttu-id="4df5e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4df5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df5e-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4df5e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df5e-130">입력</span><span class="sxs-lookup"><span data-stu-id="4df5e-130">INPUTS</span></span>

### <span data-ttu-id="4df5e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4df5e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4df5e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4df5e-132">System.String</span></span>

### <span data-ttu-id="4df5e-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4df5e-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4df5e-134">출력</span><span class="sxs-lookup"><span data-stu-id="4df5e-134">OUTPUTS</span></span>

### <span data-ttu-id="4df5e-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4df5e-135">System.Boolean</span></span>

## <span data-ttu-id="4df5e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4df5e-136">NOTES</span></span>

## <span data-ttu-id="4df5e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4df5e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4df5e-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4df5e-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="4df5e-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4df5e-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="4df5e-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="4df5e-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="4df5e-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4df5e-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="4df5e-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4df5e-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)