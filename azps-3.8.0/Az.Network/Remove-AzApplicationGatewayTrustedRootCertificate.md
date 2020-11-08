---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033800"
---
# <span data-ttu-id="4ec94-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec94-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="4ec94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec94-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec94-103">응용 프로그램 게이트웨이에서 신뢰할 수 있는 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="4ec94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ec94-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec94-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ec94-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec94-106">**AzApplicationGatewayTrustedRootCertificate** cmdlet은 기존 응용 프로그램 게이트웨이에서 신뢰할 수 있는 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="4ec94-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ec94-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec94-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ec94-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="4ec94-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="4ec94-110">두 번째 명령은 $gw에 저장 된 응용 프로그램 게이트웨이에서 myRootCA 이라는 신뢰할 수 있는 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="4ec94-111">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="4ec94-112">변수</span><span class="sxs-lookup"><span data-stu-id="4ec94-112">PARAMETERS</span></span>

### <span data-ttu-id="4ec94-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ec94-113">-ApplicationGateway</span></span>
<span data-ttu-id="4ec94-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ec94-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec94-115">-DefaultProfile</span></span>
<span data-ttu-id="4ec94-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec94-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4ec94-117">-Name</span></span>
<span data-ttu-id="4ec94-118">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec94-119">-확인</span><span class="sxs-lookup"><span data-stu-id="4ec94-119">-Confirm</span></span>
<span data-ttu-id="4ec94-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec94-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec94-121">-WhatIf</span></span>
<span data-ttu-id="4ec94-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec94-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec94-124">CommonParameters</span></span>
<span data-ttu-id="4ec94-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec94-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec94-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec94-127">입력</span><span class="sxs-lookup"><span data-stu-id="4ec94-127">INPUTS</span></span>

### <span data-ttu-id="4ec94-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ec94-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ec94-129">출력</span><span class="sxs-lookup"><span data-stu-id="4ec94-129">OUTPUTS</span></span>

### <span data-ttu-id="4ec94-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ec94-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ec94-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4ec94-131">NOTES</span></span>

## <span data-ttu-id="4ec94-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ec94-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ec94-133">추가-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec94-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4ec94-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec94-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4ec94-135">새로운 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec94-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4ec94-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec94-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)