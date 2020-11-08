---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226247"
---
# <span data-ttu-id="f449a-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f449a-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="f449a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f449a-102">SYNOPSIS</span></span>
<span data-ttu-id="f449a-103">CDN 프로필의 리소스 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f449a-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="f449a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f449a-104">SYNTAX</span></span>

### <span data-ttu-id="f449a-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f449a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f449a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f449a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f449a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f449a-107">DESCRIPTION</span></span>
<span data-ttu-id="f449a-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="f449a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f449a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f449a-109">EXAMPLES</span></span>

### <span data-ttu-id="f449a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f449a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f449a-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="f449a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f449a-112">변수</span><span class="sxs-lookup"><span data-stu-id="f449a-112">PARAMETERS</span></span>

### <span data-ttu-id="f449a-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f449a-113">-CdnProfile</span></span>
<span data-ttu-id="f449a-114">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f449a-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f449a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f449a-115">-DefaultProfile</span></span>
<span data-ttu-id="f449a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f449a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f449a-117">-/Profile</span><span class="sxs-lookup"><span data-stu-id="f449a-117">-ProfileName</span></span>
<span data-ttu-id="f449a-118">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f449a-118">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f449a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f449a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f449a-120">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f449a-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f449a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f449a-121">CommonParameters</span></span>
<span data-ttu-id="f449a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f449a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f449a-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f449a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f449a-124">입력</span><span class="sxs-lookup"><span data-stu-id="f449a-124">INPUTS</span></span>

### <span data-ttu-id="f449a-125">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f449a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f449a-126">출력</span><span class="sxs-lookup"><span data-stu-id="f449a-126">OUTPUTS</span></span>

### <span data-ttu-id="f449a-127">Microsoft. Azure. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f449a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f449a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f449a-128">NOTES</span></span>

## <span data-ttu-id="f449a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f449a-129">RELATED LINKS</span></span>