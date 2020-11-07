---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870534"
---
# <span data-ttu-id="d1474-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1474-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d1474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1474-102">SYNOPSIS</span></span>
<span data-ttu-id="d1474-103">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="d1474-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1474-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1474-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1474-105">DESCRIPTION</span></span>
<span data-ttu-id="d1474-106">**AzApplicationGatewayFrontendPort** Cmdlet은 Azure application gateway에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="d1474-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d1474-107">EXAMPLES</span></span>

### <span data-ttu-id="d1474-108">Example1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="d1474-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d1474-109">이 명령은 FrontEndPort01 이라는 프런트 엔드 포트를 포트 80에 만들고 그 결과를 $FrontEndPort 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="d1474-110">변수</span><span class="sxs-lookup"><span data-stu-id="d1474-110">PARAMETERS</span></span>

### <span data-ttu-id="d1474-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1474-111">-DefaultProfile</span></span>
<span data-ttu-id="d1474-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1474-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d1474-113">-Name</span></span>
<span data-ttu-id="d1474-114">이 cmdlet이 만드는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d1474-115">-포트</span><span class="sxs-lookup"><span data-stu-id="d1474-115">-Port</span></span>
<span data-ttu-id="d1474-116">프런트 엔드 포트의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1474-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1474-117">CommonParameters</span></span>
<span data-ttu-id="d1474-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1474-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1474-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1474-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1474-120">입력</span><span class="sxs-lookup"><span data-stu-id="d1474-120">INPUTS</span></span>

### <span data-ttu-id="d1474-121">않아야</span><span class="sxs-lookup"><span data-stu-id="d1474-121">None</span></span>

## <span data-ttu-id="d1474-122">출력</span><span class="sxs-lookup"><span data-stu-id="d1474-122">OUTPUTS</span></span>

### <span data-ttu-id="d1474-123">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d1474-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d1474-124">상속자</span><span class="sxs-lookup"><span data-stu-id="d1474-124">NOTES</span></span>

## <span data-ttu-id="d1474-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1474-125">RELATED LINKS</span></span>

[<span data-ttu-id="d1474-126">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1474-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1474-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1474-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1474-128">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1474-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1474-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1474-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)

