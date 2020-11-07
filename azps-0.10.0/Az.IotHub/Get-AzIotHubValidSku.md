---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f2d7c10e29209870d4aa6e5176731b07f7695aff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876742"
---
# <span data-ttu-id="fc258-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="fc258-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="fc258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc258-102">SYNOPSIS</span></span>
<span data-ttu-id="fc258-103">이 IotHub 전환할 수 있는 유효한 모든 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="fc258-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc258-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc258-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc258-105">DESCRIPTION</span></span>
<span data-ttu-id="fc258-106">이 IotHub 전환할 수 있는 유효한 모든 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="fc258-107">IotHub는 무료 및 유료 sku 간에 전환할 수 없으며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="fc258-108">이 작업을 수행 하려면 iothub를 삭제 하 고 다시 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="fc258-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc258-109">EXAMPLES</span></span>

### <span data-ttu-id="fc258-110">예제 1 유효한 sku 구하기</span><span class="sxs-lookup"><span data-stu-id="fc258-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fc258-111">"Myiothub" IotHub에 대 한 모든 sku 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fc258-112">변수</span><span class="sxs-lookup"><span data-stu-id="fc258-112">PARAMETERS</span></span>

### <span data-ttu-id="fc258-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc258-113">-DefaultProfile</span></span>
<span data-ttu-id="fc258-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc258-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc258-115">-이름</span><span class="sxs-lookup"><span data-stu-id="fc258-115">-Name</span></span>
<span data-ttu-id="fc258-116">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc258-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc258-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc258-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fc258-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc258-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc258-119">CommonParameters</span></span>
<span data-ttu-id="fc258-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc258-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc258-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc258-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc258-122">입력</span><span class="sxs-lookup"><span data-stu-id="fc258-122">INPUTS</span></span>

### <span data-ttu-id="fc258-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc258-123">System.String</span></span>

## <span data-ttu-id="fc258-124">출력</span><span class="sxs-lookup"><span data-stu-id="fc258-124">OUTPUTS</span></span>

### <span data-ttu-id="fc258-125">IotHub. PSIotHubSkuDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="fc258-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="fc258-126">상속자</span><span class="sxs-lookup"><span data-stu-id="fc258-126">NOTES</span></span>

## <span data-ttu-id="fc258-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc258-127">RELATED LINKS</span></span>