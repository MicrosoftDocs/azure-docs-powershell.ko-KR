---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 455ee170ffba9f601cd8e3034e0c774966f92eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875356"
---
# <span data-ttu-id="615a3-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="615a3-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="615a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="615a3-102">SYNOPSIS</span></span>
<span data-ttu-id="615a3-103">Azure application gateway에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="615a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="615a3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="615a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="615a3-105">DESCRIPTION</span></span>
<span data-ttu-id="615a3-106">Remove-AzApplicationGatewaySslPolicy cmdlet은 Azure 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="615a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="615a3-107">EXAMPLES</span></span>

### <span data-ttu-id="615a3-108">예제 1: 응용 프로그램 게이트웨이에서 SSL 정책 제거</span><span class="sxs-lookup"><span data-stu-id="615a3-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="615a3-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="615a3-110">변수</span><span class="sxs-lookup"><span data-stu-id="615a3-110">PARAMETERS</span></span>

### <span data-ttu-id="615a3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="615a3-111">-ApplicationGateway</span></span>
<span data-ttu-id="615a3-112">이 cmdlet이 SSL 정책을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="615a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615a3-113">-DefaultProfile</span></span>
<span data-ttu-id="615a3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="615a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="615a3-115">-Force</span></span>
<span data-ttu-id="615a3-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="615a3-117">-확인</span><span class="sxs-lookup"><span data-stu-id="615a3-117">-Confirm</span></span>
<span data-ttu-id="615a3-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="615a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="615a3-119">-WhatIf</span></span>
<span data-ttu-id="615a3-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="615a3-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="615a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615a3-122">CommonParameters</span></span>
<span data-ttu-id="615a3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="615a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615a3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="615a3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615a3-125">입력</span><span class="sxs-lookup"><span data-stu-id="615a3-125">INPUTS</span></span>

### <span data-ttu-id="615a3-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="615a3-126">System.String</span></span>

## <span data-ttu-id="615a3-127">출력</span><span class="sxs-lookup"><span data-stu-id="615a3-127">OUTPUTS</span></span>

### <span data-ttu-id="615a3-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="615a3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="615a3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="615a3-129">NOTES</span></span>
<span data-ttu-id="615a3-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="615a3-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="615a3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="615a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="615a3-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="615a3-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="615a3-133">새로운 AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="615a3-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="615a3-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="615a3-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)
