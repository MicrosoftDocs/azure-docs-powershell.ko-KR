---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213755"
---
# <span data-ttu-id="76097-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="76097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76097-102">SYNOPSIS</span></span>
<span data-ttu-id="76097-103">API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-103">Removes an API.</span></span>

## <span data-ttu-id="76097-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76097-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76097-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76097-105">DESCRIPTION</span></span>
<span data-ttu-id="76097-106">**Remove-AzApiManagementApi** cmdlet은 기존 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="76097-107">예제의</span><span class="sxs-lookup"><span data-stu-id="76097-107">EXAMPLES</span></span>

### <span data-ttu-id="76097-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="76097-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="76097-109">이 명령은 지정 된 ID의 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="76097-110">변수</span><span class="sxs-lookup"><span data-stu-id="76097-110">PARAMETERS</span></span>

### <span data-ttu-id="76097-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76097-111">-ApiId</span></span>
<span data-ttu-id="76097-112">API 제거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="76097-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="76097-113">-Context</span></span>
<span data-ttu-id="76097-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="76097-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76097-115">-DefaultProfile</span></span>
<span data-ttu-id="76097-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76097-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76097-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76097-117">-PassThru</span></span>
<span data-ttu-id="76097-118">passthru</span><span class="sxs-lookup"><span data-stu-id="76097-118">passthru</span></span>

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

### <span data-ttu-id="76097-119">-확인</span><span class="sxs-lookup"><span data-stu-id="76097-119">-Confirm</span></span>
<span data-ttu-id="76097-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76097-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76097-121">-WhatIf</span></span>
<span data-ttu-id="76097-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76097-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76097-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76097-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76097-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76097-124">CommonParameters</span></span>
<span data-ttu-id="76097-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76097-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76097-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76097-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76097-127">입력</span><span class="sxs-lookup"><span data-stu-id="76097-127">INPUTS</span></span>

### <span data-ttu-id="76097-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76097-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76097-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76097-129">System.String</span></span>

### <span data-ttu-id="76097-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="76097-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76097-131">출력</span><span class="sxs-lookup"><span data-stu-id="76097-131">OUTPUTS</span></span>

### <span data-ttu-id="76097-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="76097-132">System.Boolean</span></span>

## <span data-ttu-id="76097-133">상속자</span><span class="sxs-lookup"><span data-stu-id="76097-133">NOTES</span></span>

## <span data-ttu-id="76097-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76097-134">RELATED LINKS</span></span>

[<span data-ttu-id="76097-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="76097-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="76097-137">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="76097-138">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="76097-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76097-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)

