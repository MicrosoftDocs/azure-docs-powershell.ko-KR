---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204311"
---
# <span data-ttu-id="70552-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="70552-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="70552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70552-102">SYNOPSIS</span></span>
<span data-ttu-id="70552-103">이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="70552-103">Check the availability of a name.</span></span> <span data-ttu-id="70552-104">별칭: 테스트를 AzSignal.</span><span class="sxs-lookup"><span data-stu-id="70552-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="70552-105">구문과</span><span class="sxs-lookup"><span data-stu-id="70552-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70552-106">설명은</span><span class="sxs-lookup"><span data-stu-id="70552-106">DESCRIPTION</span></span>
<span data-ttu-id="70552-107">이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="70552-107">Check the availability of a name.</span></span> <span data-ttu-id="70552-108">별칭: 테스트를 AzSignal.</span><span class="sxs-lookup"><span data-stu-id="70552-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="70552-109">예제의</span><span class="sxs-lookup"><span data-stu-id="70552-109">EXAMPLES</span></span>

### <span data-ttu-id="70552-110">이름이 존재 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="70552-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="70552-111">존재 하지 않는 이름을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="70552-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="70552-112">변수</span><span class="sxs-lookup"><span data-stu-id="70552-112">PARAMETERS</span></span>

### <span data-ttu-id="70552-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70552-113">-DefaultProfile</span></span>
<span data-ttu-id="70552-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70552-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70552-115">-위치</span><span class="sxs-lookup"><span data-stu-id="70552-115">-Location</span></span>
<span data-ttu-id="70552-116">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="70552-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70552-117">-이름</span><span class="sxs-lookup"><span data-stu-id="70552-117">-Name</span></span>
<span data-ttu-id="70552-118">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70552-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="70552-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70552-119">CommonParameters</span></span>
<span data-ttu-id="70552-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70552-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70552-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70552-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70552-122">입력</span><span class="sxs-lookup"><span data-stu-id="70552-122">INPUTS</span></span>

### <span data-ttu-id="70552-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70552-123">System.String</span></span>

## <span data-ttu-id="70552-124">출력</span><span class="sxs-lookup"><span data-stu-id="70552-124">OUTPUTS</span></span>

### <span data-ttu-id="70552-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="70552-125">System.Boolean</span></span>

## <span data-ttu-id="70552-126">상속자</span><span class="sxs-lookup"><span data-stu-id="70552-126">NOTES</span></span>

## <span data-ttu-id="70552-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70552-127">RELATED LINKS</span></span>