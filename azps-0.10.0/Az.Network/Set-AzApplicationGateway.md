---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: b62a41c2c97055f0ef090ed5def3dc771ae3c1ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876625"
---
# <span data-ttu-id="eb71b-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb71b-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="eb71b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb71b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb71b-103">응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-103">Updates an application gateway.</span></span>

## <span data-ttu-id="eb71b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb71b-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb71b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb71b-105">DESCRIPTION</span></span>
<span data-ttu-id="eb71b-106">**AzApplicationGateway** Cmdlet은 Azure application gateway를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="eb71b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eb71b-107">EXAMPLES</span></span>

### <span data-ttu-id="eb71b-108">예제 1: 응용 프로그램 게이트웨이 업데이트</span><span class="sxs-lookup"><span data-stu-id="eb71b-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="eb71b-109">이 명령은 $AppGw 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이를 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="eb71b-110">변수</span><span class="sxs-lookup"><span data-stu-id="eb71b-110">PARAMETERS</span></span>

### <span data-ttu-id="eb71b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb71b-111">-ApplicationGateway</span></span>
<span data-ttu-id="eb71b-112">응용 프로그램 게이트웨이를 설정 해야 하는 상태를 나타내는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="eb71b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb71b-113">-AsJob</span></span>
<span data-ttu-id="eb71b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eb71b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb71b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb71b-115">-DefaultProfile</span></span>
<span data-ttu-id="eb71b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb71b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb71b-117">CommonParameters</span></span>
<span data-ttu-id="eb71b-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb71b-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb71b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb71b-120">입력</span><span class="sxs-lookup"><span data-stu-id="eb71b-120">INPUTS</span></span>

### <span data-ttu-id="eb71b-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb71b-121">PSApplicationGateway</span></span>
<span data-ttu-id="eb71b-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb71b-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="eb71b-123">출력</span><span class="sxs-lookup"><span data-stu-id="eb71b-123">OUTPUTS</span></span>

### <span data-ttu-id="eb71b-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb71b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb71b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="eb71b-125">NOTES</span></span>

## <span data-ttu-id="eb71b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb71b-126">RELATED LINKS</span></span>

[<span data-ttu-id="eb71b-127">시작-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb71b-127">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)

