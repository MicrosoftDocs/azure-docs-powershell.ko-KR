---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876015"
---
# <span data-ttu-id="c1242-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="c1242-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="c1242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1242-102">SYNOPSIS</span></span>
<span data-ttu-id="c1242-103">저장소 리소스 공급자 설정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="c1242-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1242-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1242-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1242-105">DESCRIPTION</span></span>
<span data-ttu-id="c1242-106">저장소 리소스 공급자 설정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="c1242-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1242-107">EXAMPLES</span></span>

### <span data-ttu-id="c1242-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="c1242-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="c1242-109">저장소 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-109">Get the storage settings.</span></span>

## <span data-ttu-id="c1242-110">변수</span><span class="sxs-lookup"><span data-stu-id="c1242-110">PARAMETERS</span></span>

### <span data-ttu-id="c1242-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1242-111">-DefaultProfile</span></span>
<span data-ttu-id="c1242-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1242-113">-위치</span><span class="sxs-lookup"><span data-stu-id="c1242-113">-Location</span></span>
<span data-ttu-id="c1242-114">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1242-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1242-115">-SubscriptionId</span></span>
<span data-ttu-id="c1242-116">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1242-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1242-117">CommonParameters</span></span>
<span data-ttu-id="c1242-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1242-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1242-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1242-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1242-120">입력</span><span class="sxs-lookup"><span data-stu-id="c1242-120">INPUTS</span></span>

## <span data-ttu-id="c1242-121">출력</span><span class="sxs-lookup"><span data-stu-id="c1242-121">OUTPUTS</span></span>

### <span data-ttu-id="c1242-122">Api201908Preview on. i i m. i a i 설정</span><span class="sxs-lookup"><span data-stu-id="c1242-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="c1242-123">상속자</span><span class="sxs-lookup"><span data-stu-id="c1242-123">NOTES</span></span>

## <span data-ttu-id="c1242-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1242-124">RELATED LINKS</span></span>
