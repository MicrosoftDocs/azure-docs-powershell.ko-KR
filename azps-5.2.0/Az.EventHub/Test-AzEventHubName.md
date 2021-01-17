---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345326"
---
# <span data-ttu-id="9216a-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="9216a-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="9216a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9216a-102">SYNOPSIS</span></span>
<span data-ttu-id="9216a-103">주어진 NameSpace 이름 또는 별칭(DR 구성 이름)의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9216a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9216a-104">SYNTAX</span></span>

### <span data-ttu-id="9216a-105">NamespaceCheckNameAvailabilitySet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9216a-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9216a-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9216a-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9216a-107">설명</span><span class="sxs-lookup"><span data-stu-id="9216a-107">DESCRIPTION</span></span>
<span data-ttu-id="9216a-108">**Test-AzEventhubName** Cmdlet은 NameSpace 이름 또는 별칭(DR 구성 이름)의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9216a-109">예제</span><span class="sxs-lookup"><span data-stu-id="9216a-109">EXAMPLES</span></span>

### <span data-ttu-id="9216a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9216a-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="9216a-111">사용 가능한 경우 네임스페이스 이름 'MyNameSapceName'의 가용성 상태를 True로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="9216a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9216a-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="9216a-113">'MyNameSapceName' 네임스페이스 이름의 가용성에 대한 상태를 이유로 False로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="9216a-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="9216a-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="9216a-115">사용 가능한 경우 'MyNameSapceName' 네임스페이스에 대한 별칭 이름 'myAliasName'의 가용성 상태를 True로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="9216a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9216a-116">PARAMETERS</span></span>

### <span data-ttu-id="9216a-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9216a-117">-AliasName</span></span>
<span data-ttu-id="9216a-118">DR 구성 이름 - 별칭 이름</span><span class="sxs-lookup"><span data-stu-id="9216a-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9216a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9216a-119">-DefaultProfile</span></span>
<span data-ttu-id="9216a-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9216a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9216a-121">-Namespace</span></span>
<span data-ttu-id="9216a-122">Eventhub 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="9216a-122">Eventhub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9216a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9216a-123">-ResourceGroupName</span></span>
<span data-ttu-id="9216a-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9216a-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9216a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9216a-125">CommonParameters</span></span>
<span data-ttu-id="9216a-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9216a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9216a-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9216a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9216a-128">입력</span><span class="sxs-lookup"><span data-stu-id="9216a-128">INPUTS</span></span>

### <span data-ttu-id="9216a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9216a-129">System.String</span></span>

## <span data-ttu-id="9216a-130">출력</span><span class="sxs-lookup"><span data-stu-id="9216a-130">OUTPUTS</span></span>

### <span data-ttu-id="9216a-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="9216a-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="9216a-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9216a-132">NOTES</span></span>

## <span data-ttu-id="9216a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9216a-133">RELATED LINKS</span></span>