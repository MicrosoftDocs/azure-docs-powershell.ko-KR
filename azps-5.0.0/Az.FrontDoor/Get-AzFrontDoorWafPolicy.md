---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215456"
---
# <span data-ttu-id="55ead-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="55ead-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="55ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ead-102">SYNOPSIS</span></span>
<span data-ttu-id="55ead-103">WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="55ead-103">Get WAF policy</span></span>

## <span data-ttu-id="55ead-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55ead-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ead-105">설명은</span><span class="sxs-lookup"><span data-stu-id="55ead-105">DESCRIPTION</span></span>
<span data-ttu-id="55ead-106">**AzFrontDoorWafPolicy** cmdletget은 현재 구독 아래의 리소스 그룹에서 waf 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="55ead-107">예제의</span><span class="sxs-lookup"><span data-stu-id="55ead-107">EXAMPLES</span></span>

### <span data-ttu-id="55ead-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="55ead-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="55ead-109">$resourceGroupName에 $policyName 이라는 WAF 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="55ead-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="55ead-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="55ead-111">$resourceGroupName에서 모든 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="55ead-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="55ead-112">변수</span><span class="sxs-lookup"><span data-stu-id="55ead-112">PARAMETERS</span></span>

### <span data-ttu-id="55ead-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ead-113">-DefaultProfile</span></span>
<span data-ttu-id="55ead-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ead-115">-이름</span><span class="sxs-lookup"><span data-stu-id="55ead-115">-Name</span></span>
<span data-ttu-id="55ead-116">FireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ead-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ead-117">-ResourceGroupName</span></span>
<span data-ttu-id="55ead-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-118">The resource group name.</span></span>

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

### <span data-ttu-id="55ead-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ead-119">CommonParameters</span></span>
<span data-ttu-id="55ead-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ead-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ead-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55ead-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ead-122">입력</span><span class="sxs-lookup"><span data-stu-id="55ead-122">INPUTS</span></span>

### <span data-ttu-id="55ead-123">않아야</span><span class="sxs-lookup"><span data-stu-id="55ead-123">None</span></span>

## <span data-ttu-id="55ead-124">출력</span><span class="sxs-lookup"><span data-stu-id="55ead-124">OUTPUTS</span></span>

### <span data-ttu-id="55ead-125">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="55ead-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="55ead-126">상속자</span><span class="sxs-lookup"><span data-stu-id="55ead-126">NOTES</span></span>

## <span data-ttu-id="55ead-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55ead-127">RELATED LINKS</span></span>

<span data-ttu-id="55ead-128">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [업데이트-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [제거-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="55ead-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>