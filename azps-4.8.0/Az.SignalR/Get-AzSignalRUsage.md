---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047586"
---
# <span data-ttu-id="3bcef-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="3bcef-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="3bcef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bcef-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcef-103">구독의 사용 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="3bcef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bcef-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bcef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3bcef-105">DESCRIPTION</span></span>
<span data-ttu-id="3bcef-106">구독의 사용 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="3bcef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3bcef-107">EXAMPLES</span></span>

### <span data-ttu-id="3bcef-108">위치를 입력 하 여 사용 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="3bcef-109">변수</span><span class="sxs-lookup"><span data-stu-id="3bcef-109">PARAMETERS</span></span>

### <span data-ttu-id="3bcef-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcef-110">-DefaultProfile</span></span>
<span data-ttu-id="3bcef-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bcef-112">-위치</span><span class="sxs-lookup"><span data-stu-id="3bcef-112">-Location</span></span>
<span data-ttu-id="3bcef-113">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcef-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcef-114">CommonParameters</span></span>
<span data-ttu-id="3bcef-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bcef-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcef-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3bcef-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcef-117">입력</span><span class="sxs-lookup"><span data-stu-id="3bcef-117">INPUTS</span></span>

### <span data-ttu-id="3bcef-118">않아야</span><span class="sxs-lookup"><span data-stu-id="3bcef-118">None</span></span>

## <span data-ttu-id="3bcef-119">출력</span><span class="sxs-lookup"><span data-stu-id="3bcef-119">OUTPUTS</span></span>

### <span data-ttu-id="3bcef-120">SignalR. PSSignalRUsage/.</span><span class="sxs-lookup"><span data-stu-id="3bcef-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="3bcef-121">상속자</span><span class="sxs-lookup"><span data-stu-id="3bcef-121">NOTES</span></span>

## <span data-ttu-id="3bcef-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bcef-122">RELATED LINKS</span></span>