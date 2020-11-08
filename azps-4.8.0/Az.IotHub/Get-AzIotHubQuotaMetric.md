---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211962"
---
# <span data-ttu-id="48ba8-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="48ba8-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="48ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="48ba8-103">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48ba8-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="48ba8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48ba8-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ba8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="48ba8-106">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48ba8-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="48ba8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="48ba8-108">예제 1 할당량 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="48ba8-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="48ba8-109">"Myiothub" IotHub에 대 한 할당량 메트릭 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48ba8-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="48ba8-110">변수</span><span class="sxs-lookup"><span data-stu-id="48ba8-110">PARAMETERS</span></span>

### <span data-ttu-id="48ba8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ba8-111">-DefaultProfile</span></span>
<span data-ttu-id="48ba8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48ba8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48ba8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="48ba8-113">-Name</span></span>
<span data-ttu-id="48ba8-114">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48ba8-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="48ba8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ba8-115">-ResourceGroupName</span></span>
<span data-ttu-id="48ba8-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="48ba8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="48ba8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ba8-117">CommonParameters</span></span>
<span data-ttu-id="48ba8-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48ba8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ba8-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ba8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ba8-120">입력</span><span class="sxs-lookup"><span data-stu-id="48ba8-120">INPUTS</span></span>

### <span data-ttu-id="48ba8-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48ba8-121">System.String</span></span>

## <span data-ttu-id="48ba8-122">출력</span><span class="sxs-lookup"><span data-stu-id="48ba8-122">OUTPUTS</span></span>

### <span data-ttu-id="48ba8-123">IotHub. PSIotHubQuotaMetric/. \*</span><span class="sxs-lookup"><span data-stu-id="48ba8-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="48ba8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="48ba8-124">NOTES</span></span>

## <span data-ttu-id="48ba8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48ba8-125">RELATED LINKS</span></span>