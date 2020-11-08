---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 4909c9d9b9a7fa1af1e4353c63256ed73d229f57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042154"
---
# <span data-ttu-id="ae628-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ae628-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ae628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae628-102">SYNOPSIS</span></span>
<span data-ttu-id="ae628-103">기존 Id 공급자 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="ae628-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae628-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae628-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae628-105">DESCRIPTION</span></span>
<span data-ttu-id="ae628-106">기존 Id 공급자 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="ae628-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae628-107">EXAMPLES</span></span>

### <span data-ttu-id="ae628-108">ApiManagement 서비스에서 Facebook id 공급자 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="ae628-109">Facebook Id 공급자 구성과 관련 된 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="ae628-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae628-110">PARAMETERS</span></span>

### <span data-ttu-id="ae628-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ae628-111">-Context</span></span>
<span data-ttu-id="ae628-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ae628-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ae628-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae628-114">-DefaultProfile</span></span>
<span data-ttu-id="ae628-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae628-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae628-116">-PassThru</span></span>
<span data-ttu-id="ae628-117">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="ae628-118">-Type</span><span class="sxs-lookup"><span data-stu-id="ae628-118">-Type</span></span>
<span data-ttu-id="ae628-119">기존 Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="ae628-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae628-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ae628-121">-Confirm</span></span>
<span data-ttu-id="ae628-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae628-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae628-123">-WhatIf</span></span>
<span data-ttu-id="ae628-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae628-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae628-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae628-126">CommonParameters</span></span>
<span data-ttu-id="ae628-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae628-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae628-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae628-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae628-129">입력</span><span class="sxs-lookup"><span data-stu-id="ae628-129">INPUTS</span></span>

### <span data-ttu-id="ae628-130">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae628-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae628-131">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="ae628-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="ae628-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae628-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae628-133">출력</span><span class="sxs-lookup"><span data-stu-id="ae628-133">OUTPUTS</span></span>

### <span data-ttu-id="ae628-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ae628-134">System.Boolean</span></span>

## <span data-ttu-id="ae628-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ae628-135">NOTES</span></span>

## <span data-ttu-id="ae628-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae628-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae628-137">새로운 AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ae628-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="ae628-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ae628-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="ae628-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ae628-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
