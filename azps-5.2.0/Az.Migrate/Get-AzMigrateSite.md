---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356812"
---
# <span data-ttu-id="ecc5a-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="ecc5a-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="ecc5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc5a-103">사이트를 얻을 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-103">Method to get a site.</span></span>

## <span data-ttu-id="ecc5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecc5a-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ecc5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc5a-106">사이트를 얻을 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-106">Method to get a site.</span></span>

## <span data-ttu-id="ecc5a-107">예제</span><span class="sxs-lookup"><span data-stu-id="ecc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc5a-108">예제 1: Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="ecc5a-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="ecc5a-109">이름으로 사이트 얻기</span><span class="sxs-lookup"><span data-stu-id="ecc5a-109">Get site by name</span></span>

## <span data-ttu-id="ecc5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc5a-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc5a-111">-DefaultProfile</span></span>
<span data-ttu-id="ecc5a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc5a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ecc5a-113">-Name</span></span>
<span data-ttu-id="ecc5a-114">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ecc5a-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-116">The name of the resource group.</span></span>
<span data-ttu-id="ecc5a-117">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ecc5a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecc5a-118">-SubscriptionId</span></span>
<span data-ttu-id="ecc5a-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ecc5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc5a-120">CommonParameters</span></span>
<span data-ttu-id="ecc5a-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc5a-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc5a-123">입력</span><span class="sxs-lookup"><span data-stu-id="ecc5a-123">INPUTS</span></span>

## <span data-ttu-id="ecc5a-124">출력</span><span class="sxs-lookup"><span data-stu-id="ecc5a-124">OUTPUTS</span></span>

### <span data-ttu-id="ecc5a-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="ecc5a-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="ecc5a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecc5a-126">NOTES</span></span>

<span data-ttu-id="ecc5a-127">별칭</span><span class="sxs-lookup"><span data-stu-id="ecc5a-127">ALIASES</span></span>

## <span data-ttu-id="ecc5a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecc5a-128">RELATED LINKS</span></span>
