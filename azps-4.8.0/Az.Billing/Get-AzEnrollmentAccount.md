---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056771"
---
# <span data-ttu-id="05209-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="05209-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="05209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05209-102">SYNOPSIS</span></span>
<span data-ttu-id="05209-103">등록 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="05209-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="05209-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05209-104">SYNTAX</span></span>

### <span data-ttu-id="05209-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="05209-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05209-106">단일</span><span class="sxs-lookup"><span data-stu-id="05209-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05209-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05209-107">DESCRIPTION</span></span>
<span data-ttu-id="05209-108">**Get-AzEnrollmentAccount** cmdlet은 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05209-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="05209-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05209-109">EXAMPLES</span></span>

### <span data-ttu-id="05209-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05209-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="05209-111">사용 가능한 모든 등록 계정을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="05209-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="05209-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="05209-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="05209-113">지정 된 개체 id를 사용 하 여 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05209-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="05209-114">변수</span><span class="sxs-lookup"><span data-stu-id="05209-114">PARAMETERS</span></span>

### <span data-ttu-id="05209-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05209-115">-DefaultProfile</span></span>
<span data-ttu-id="05209-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="05209-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05209-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="05209-117">-ObjectId</span></span>
<span data-ttu-id="05209-118">가져올 특정 등록 계정의 ObjectId.</span><span class="sxs-lookup"><span data-stu-id="05209-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05209-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05209-119">CommonParameters</span></span>
<span data-ttu-id="05209-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05209-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05209-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05209-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05209-122">입력</span><span class="sxs-lookup"><span data-stu-id="05209-122">INPUTS</span></span>

### <span data-ttu-id="05209-123">않아야</span><span class="sxs-lookup"><span data-stu-id="05209-123">None</span></span>

## <span data-ttu-id="05209-124">출력</span><span class="sxs-lookup"><span data-stu-id="05209-124">OUTPUTS</span></span>

### <span data-ttu-id="05209-125">PSBillingPeriod를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="05209-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="05209-126">상속자</span><span class="sxs-lookup"><span data-stu-id="05209-126">NOTES</span></span>

## <span data-ttu-id="05209-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05209-127">RELATED LINKS</span></span>