---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213981"
---
# <span data-ttu-id="8af52-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="8af52-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="8af52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af52-102">SYNOPSIS</span></span>
<span data-ttu-id="8af52-103">Iot 보안 솔루션에 대 한 새 사용자 정의 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="8af52-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="8af52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8af52-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8af52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8af52-105">DESCRIPTION</span></span>
<span data-ttu-id="8af52-106">AzIotSecuritySolutionUserDefinedResourcesObject cmdlet은 iot security 솔루션에 대 한 새 사용자 정의 리소스 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8af52-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="8af52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8af52-107">EXAMPLES</span></span>

### <span data-ttu-id="8af52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8af52-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="8af52-109">새 사용자 정의 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="8af52-109">Create new user defined resources</span></span>

## <span data-ttu-id="8af52-110">변수</span><span class="sxs-lookup"><span data-stu-id="8af52-110">PARAMETERS</span></span>

### <span data-ttu-id="8af52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af52-111">-DefaultProfile</span></span>
<span data-ttu-id="8af52-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8af52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af52-113">-쿼리</span><span class="sxs-lookup"><span data-stu-id="8af52-113">-Query</span></span>
<span data-ttu-id="8af52-114">쿼리.</span><span class="sxs-lookup"><span data-stu-id="8af52-114">Query.</span></span>

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

### <span data-ttu-id="8af52-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="8af52-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="8af52-116">쿼리 구독</span><span class="sxs-lookup"><span data-stu-id="8af52-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af52-117">CommonParameters</span></span>
<span data-ttu-id="8af52-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af52-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8af52-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af52-120">입력</span><span class="sxs-lookup"><span data-stu-id="8af52-120">INPUTS</span></span>

### <span data-ttu-id="8af52-121">않아야</span><span class="sxs-lookup"><span data-stu-id="8af52-121">None</span></span>

## <span data-ttu-id="8af52-122">출력</span><span class="sxs-lookup"><span data-stu-id="8af52-122">OUTPUTS</span></span>

### <span data-ttu-id="8af52-123">Microsoft. Azure. IPSUserDefinedResources Securitysolutions.</span><span class="sxs-lookup"><span data-stu-id="8af52-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="8af52-124">상속자</span><span class="sxs-lookup"><span data-stu-id="8af52-124">NOTES</span></span>

## <span data-ttu-id="8af52-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8af52-125">RELATED LINKS</span></span>