---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217595"
---
# <span data-ttu-id="b9c77-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b9c77-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="b9c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c77-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c77-103">수정 된 방화벽을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="b9c77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9c77-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9c77-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c77-106">**AzIpGroup** Cmdlet은 Azure ipgroup을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="b9c77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b9c77-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9c77-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="b9c77-109">변수</span><span class="sxs-lookup"><span data-stu-id="b9c77-109">PARAMETERS</span></span>

### <span data-ttu-id="b9c77-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9c77-110">-AsJob</span></span>
<span data-ttu-id="b9c77-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b9c77-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c77-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c77-112">-DefaultProfile</span></span>
<span data-ttu-id="b9c77-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c77-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="b9c77-114">-IpGroup</span></span>
<span data-ttu-id="b9c77-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="b9c77-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c77-116">-확인</span><span class="sxs-lookup"><span data-stu-id="b9c77-116">-Confirm</span></span>
<span data-ttu-id="b9c77-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c77-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c77-118">-WhatIf</span></span>
<span data-ttu-id="b9c77-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c77-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c77-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c77-121">CommonParameters</span></span>
<span data-ttu-id="b9c77-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c77-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c77-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9c77-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c77-124">입력</span><span class="sxs-lookup"><span data-stu-id="b9c77-124">INPUTS</span></span>

### <span data-ttu-id="b9c77-125">PSIpGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b9c77-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="b9c77-126">출력</span><span class="sxs-lookup"><span data-stu-id="b9c77-126">OUTPUTS</span></span>

### <span data-ttu-id="b9c77-127">PSIpGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b9c77-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="b9c77-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b9c77-128">NOTES</span></span>

## <span data-ttu-id="b9c77-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c77-129">RELATED LINKS</span></span>