---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351237"
---
# <span data-ttu-id="6aeb4-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6aeb4-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="6aeb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="6aeb4-103">청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-103">Get billing accounts.</span></span>

## <span data-ttu-id="6aeb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="6aeb4-104">SYNTAX</span></span>

### <span data-ttu-id="6aeb4-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="6aeb4-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aeb4-106">Single</span><span class="sxs-lookup"><span data-stu-id="6aeb4-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aeb4-107">설명</span><span class="sxs-lookup"><span data-stu-id="6aeb4-107">DESCRIPTION</span></span>
<span data-ttu-id="6aeb4-108">**Get-AzBillingAccount** cmdlet은 청구 계정을, 사용자가 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="6aeb4-109">예제</span><span class="sxs-lookup"><span data-stu-id="6aeb4-109">EXAMPLES</span></span>

### <span data-ttu-id="6aeb4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6aeb4-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="6aeb4-111">사용자가 액세스할 수 있는 모든 청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="6aeb4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6aeb4-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6aeb4-113">지정된 이름으로 청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="6aeb4-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="6aeb4-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="6aeb4-115">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 주소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="6aeb4-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="6aeb4-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="6aeb4-117">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 청구 프로필을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="6aeb4-118">예제 5</span><span class="sxs-lookup"><span data-stu-id="6aeb4-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="6aeb4-119">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 청구 프로필 및 청구서 섹션을 결과에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="6aeb4-120">예제 6</span><span class="sxs-lookup"><span data-stu-id="6aeb4-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6aeb4-121">지정된 이름의 청구 계정을 얻게 하여 주소, 청구 프로필 및 송장 섹션을 결과에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="6aeb4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aeb4-122">PARAMETERS</span></span>

### <span data-ttu-id="6aeb4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aeb4-123">-DefaultProfile</span></span>
<span data-ttu-id="6aeb4-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6aeb4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6aeb4-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="6aeb4-125">-IncludeAddress</span></span>
<span data-ttu-id="6aeb4-126">청구 계정의 주소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-126">Include the address of the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeb4-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="6aeb4-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="6aeb4-128">청구 계정 아래에 청구 프로필을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-128">Include the billing profiles under the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeb4-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="6aeb4-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="6aeb4-130">청구 계정 아래에 청구 프로필 및 청구서 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeb4-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6aeb4-131">-Name</span></span>
<span data-ttu-id="6aeb4-132">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeb4-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="6aeb4-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="6aeb4-134">구독을 만드는 데 입력으로 사용할 수 있는 청구 계정 아래에 청구 엔터티를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aeb4-135">CommonParameters</span></span>
<span data-ttu-id="6aeb4-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aeb4-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6aeb4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aeb4-138">입력</span><span class="sxs-lookup"><span data-stu-id="6aeb4-138">INPUTS</span></span>

### <span data-ttu-id="6aeb4-139">없음</span><span class="sxs-lookup"><span data-stu-id="6aeb4-139">None</span></span>

## <span data-ttu-id="6aeb4-140">출력</span><span class="sxs-lookup"><span data-stu-id="6aeb4-140">OUTPUTS</span></span>

### <span data-ttu-id="6aeb4-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6aeb4-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="6aeb4-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6aeb4-142">NOTES</span></span>

## <span data-ttu-id="6aeb4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aeb4-143">RELATED LINKS</span></span>