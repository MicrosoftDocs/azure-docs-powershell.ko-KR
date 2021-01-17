---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327417"
---
# <span data-ttu-id="b6ac7-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b6ac7-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="b6ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ac7-103">지정된 Relay 네임스페이스에서 WcfRelay를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="b6ac7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6ac7-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ac7-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ac7-106">**Remove-AzWcfRelay** cmdlet은 지정된 Relay 네임스페이스에서 WcfRelay를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="b6ac7-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ac7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6ac7-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="b6ac7-109">네임스페이스에서 WcfRelay를 `TestWCFRelay1` `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b6ac7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ac7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ac7-111">-DefaultProfile</span></span>
<span data-ttu-id="b6ac7-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ac7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b6ac7-113">-Name</span></span>
<span data-ttu-id="b6ac7-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ac7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6ac7-115">-Namespace</span></span>
<span data-ttu-id="b6ac7-116">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ac7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ac7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6ac7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6ac7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6ac7-119">-Confirm</span></span>
<span data-ttu-id="b6ac7-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ac7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ac7-121">-WhatIf</span></span>
<span data-ttu-id="b6ac7-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6ac7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ac7-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ac7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ac7-124">CommonParameters</span></span>
<span data-ttu-id="b6ac7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ac7-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6ac7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ac7-127">입력</span><span class="sxs-lookup"><span data-stu-id="b6ac7-127">INPUTS</span></span>

### <span data-ttu-id="b6ac7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b6ac7-128">System.String</span></span>

## <span data-ttu-id="b6ac7-129">출력</span><span class="sxs-lookup"><span data-stu-id="b6ac7-129">OUTPUTS</span></span>

### <span data-ttu-id="b6ac7-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="b6ac7-130">System.Void</span></span>

## <span data-ttu-id="b6ac7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6ac7-131">NOTES</span></span>

## <span data-ttu-id="b6ac7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6ac7-132">RELATED LINKS</span></span>