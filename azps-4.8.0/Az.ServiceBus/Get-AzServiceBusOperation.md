---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047621"
---
# <span data-ttu-id="1008b-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="1008b-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="1008b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1008b-102">SYNOPSIS</span></span>
<span data-ttu-id="1008b-103">지원 되는 ServiceBus 작업 나열</span><span class="sxs-lookup"><span data-stu-id="1008b-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="1008b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1008b-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1008b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1008b-105">DESCRIPTION</span></span>
<span data-ttu-id="1008b-106">**AzServiceBusOperation** cmdlet에는 ServiceBus 지원 되는 작업이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1008b-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="1008b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1008b-107">EXAMPLES</span></span>

### <span data-ttu-id="1008b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1008b-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="1008b-109">ServiceBus 지원 되는 작업 나열</span><span class="sxs-lookup"><span data-stu-id="1008b-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="1008b-110">변수</span><span class="sxs-lookup"><span data-stu-id="1008b-110">PARAMETERS</span></span>

### <span data-ttu-id="1008b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1008b-111">-DefaultProfile</span></span>
<span data-ttu-id="1008b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1008b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1008b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1008b-113">CommonParameters</span></span>
<span data-ttu-id="1008b-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1008b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1008b-115">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1008b-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1008b-116">입력</span><span class="sxs-lookup"><span data-stu-id="1008b-116">INPUTS</span></span>

### <span data-ttu-id="1008b-117">않아야</span><span class="sxs-lookup"><span data-stu-id="1008b-117">None</span></span>

## <span data-ttu-id="1008b-118">출력</span><span class="sxs-lookup"><span data-stu-id="1008b-118">OUTPUTS</span></span>

### <span data-ttu-id="1008b-119">ServiceBus. PSOperationAttributes/.</span><span class="sxs-lookup"><span data-stu-id="1008b-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="1008b-120">상속자</span><span class="sxs-lookup"><span data-stu-id="1008b-120">NOTES</span></span>

## <span data-ttu-id="1008b-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1008b-121">RELATED LINKS</span></span>