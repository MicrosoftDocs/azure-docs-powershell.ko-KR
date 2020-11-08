---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218243"
---
# <span data-ttu-id="58c5d-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="58c5d-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="58c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="58c5d-103">개인 링크 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="58c5d-103">Removes a private link service</span></span>

## <span data-ttu-id="58c5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58c5d-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="58c5d-106">**AzPrivateLinkService** cmdlet는 개인 링크 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="58c5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="58c5d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="58c5d-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="58c5d-109">이 예제에서는 TestPrivateLinkService 이라는 개인 링크 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="58c5d-110">변수</span><span class="sxs-lookup"><span data-stu-id="58c5d-110">PARAMETERS</span></span>

### <span data-ttu-id="58c5d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58c5d-111">-AsJob</span></span>
<span data-ttu-id="58c5d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="58c5d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58c5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c5d-113">-DefaultProfile</span></span>
<span data-ttu-id="58c5d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c5d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="58c5d-115">-Force</span></span>
<span data-ttu-id="58c5d-116">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="58c5d-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="58c5d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="58c5d-117">-Name</span></span>
<span data-ttu-id="58c5d-118">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c5d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58c5d-119">-PassThru</span></span>
<span data-ttu-id="58c5d-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58c5d-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58c5d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c5d-122">-ResourceGroupName</span></span>
<span data-ttu-id="58c5d-123">개인 링크 서비스의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c5d-124">-확인</span><span class="sxs-lookup"><span data-stu-id="58c5d-124">-Confirm</span></span>
<span data-ttu-id="58c5d-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c5d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c5d-126">-WhatIf</span></span>
<span data-ttu-id="58c5d-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c5d-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c5d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c5d-129">CommonParameters</span></span>
<span data-ttu-id="58c5d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c5d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c5d-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58c5d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c5d-132">입력</span><span class="sxs-lookup"><span data-stu-id="58c5d-132">INPUTS</span></span>

### <span data-ttu-id="58c5d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58c5d-133">System.String</span></span>

## <span data-ttu-id="58c5d-134">출력</span><span class="sxs-lookup"><span data-stu-id="58c5d-134">OUTPUTS</span></span>

### <span data-ttu-id="58c5d-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="58c5d-135">System.Boolean</span></span>

## <span data-ttu-id="58c5d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="58c5d-136">NOTES</span></span>

## <span data-ttu-id="58c5d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58c5d-137">RELATED LINKS</span></span>

[<span data-ttu-id="58c5d-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="58c5d-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="58c5d-139">새로운 AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="58c5d-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)