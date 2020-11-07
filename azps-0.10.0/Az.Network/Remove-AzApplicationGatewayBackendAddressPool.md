---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a9346f3ff990007ed1033032d111e5851a2ac534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875377"
---
# <span data-ttu-id="63e6c-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e6c-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="63e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="63e6c-103">응용 프로그램 게이트웨이에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="63e6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63e6c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="63e6c-106">**AzApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="63e6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="63e6c-108">예제 1: 응용 프로그램 게이트웨이에서 백 엔드 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="63e6c-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="63e6c-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="63e6c-110">두 번째 명령은 응용 프로그램 게이트웨이에서 BackEndPool02 이라는 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="63e6c-111">변수</span><span class="sxs-lookup"><span data-stu-id="63e6c-111">PARAMETERS</span></span>

### <span data-ttu-id="63e6c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63e6c-112">-ApplicationGateway</span></span>
<span data-ttu-id="63e6c-113">이 cmdlet이 백 엔드 주소 풀을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e6c-114">-DefaultProfile</span></span>
<span data-ttu-id="63e6c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e6c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="63e6c-116">-Name</span></span>
<span data-ttu-id="63e6c-117">이 cmdlet이 제거 하는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e6c-118">-확인</span><span class="sxs-lookup"><span data-stu-id="63e6c-118">-Confirm</span></span>
<span data-ttu-id="63e6c-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e6c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e6c-120">-WhatIf</span></span>
<span data-ttu-id="63e6c-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e6c-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e6c-123">CommonParameters</span></span>
<span data-ttu-id="63e6c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e6c-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e6c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e6c-126">입력</span><span class="sxs-lookup"><span data-stu-id="63e6c-126">INPUTS</span></span>

### <span data-ttu-id="63e6c-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63e6c-127">System.String</span></span>

## <span data-ttu-id="63e6c-128">출력</span><span class="sxs-lookup"><span data-stu-id="63e6c-128">OUTPUTS</span></span>

### <span data-ttu-id="63e6c-129">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63e6c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="63e6c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="63e6c-130">NOTES</span></span>

## <span data-ttu-id="63e6c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63e6c-131">RELATED LINKS</span></span>

[<span data-ttu-id="63e6c-132">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e6c-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63e6c-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e6c-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63e6c-134">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e6c-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63e6c-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e6c-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

