---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350157"
---
# <span data-ttu-id="53e9e-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="53e9e-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="53e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="53e9e-103">지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="53e9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="53e9e-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53e9e-105">설명</span><span class="sxs-lookup"><span data-stu-id="53e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="53e9e-106">**Remove-AzRelayNamespace** cmdlet은 지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="53e9e-107">예제</span><span class="sxs-lookup"><span data-stu-id="53e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="53e9e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="53e9e-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="53e9e-109">지정된 리소스 그룹에서 릴레이 `TestNameSpace-Relay1` 네임스페이스를 `Default-ServiceBus-WestUS` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="53e9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53e9e-110">PARAMETERS</span></span>

### <span data-ttu-id="53e9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e9e-111">-DefaultProfile</span></span>
<span data-ttu-id="53e9e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53e9e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="53e9e-113">-Name</span></span>
<span data-ttu-id="53e9e-114">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="53e9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53e9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="53e9e-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="53e9e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53e9e-117">-Confirm</span></span>
<span data-ttu-id="53e9e-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53e9e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53e9e-119">-WhatIf</span></span>
<span data-ttu-id="53e9e-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53e9e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53e9e-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53e9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e9e-122">CommonParameters</span></span>
<span data-ttu-id="53e9e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53e9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e9e-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="53e9e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e9e-125">입력</span><span class="sxs-lookup"><span data-stu-id="53e9e-125">INPUTS</span></span>

### <span data-ttu-id="53e9e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="53e9e-126">System.String</span></span>

## <span data-ttu-id="53e9e-127">출력</span><span class="sxs-lookup"><span data-stu-id="53e9e-127">OUTPUTS</span></span>

### <span data-ttu-id="53e9e-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="53e9e-128">System.Void</span></span>

## <span data-ttu-id="53e9e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53e9e-129">NOTES</span></span>

## <span data-ttu-id="53e9e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53e9e-130">RELATED LINKS</span></span>