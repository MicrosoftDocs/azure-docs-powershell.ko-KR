---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345494"
---
# <span data-ttu-id="918f0-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="918f0-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="918f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="918f0-102">SYNOPSIS</span></span>
<span data-ttu-id="918f0-103">방화벽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-103">Remove a Firewall.</span></span>

## <span data-ttu-id="918f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="918f0-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="918f0-105">설명</span><span class="sxs-lookup"><span data-stu-id="918f0-105">DESCRIPTION</span></span>
<span data-ttu-id="918f0-106">**Remove-AzFirewall** cmdlet은 Azure Firewall을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="918f0-107">예제</span><span class="sxs-lookup"><span data-stu-id="918f0-107">EXAMPLES</span></span>

### <span data-ttu-id="918f0-108">예제 1: 방화벽 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="918f0-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="918f0-109">이 예제에서는 방화벽을 만든 다음 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="918f0-110">방화벽을 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="918f0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="918f0-111">PARAMETERS</span></span>

### <span data-ttu-id="918f0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="918f0-112">-AsJob</span></span>
<span data-ttu-id="918f0-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="918f0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="918f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918f0-114">-DefaultProfile</span></span>
<span data-ttu-id="918f0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="918f0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="918f0-116">-Force</span></span>
<span data-ttu-id="918f0-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="918f0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="918f0-118">-Name</span></span>
<span data-ttu-id="918f0-119">이 cmdlet이 제거하는 방화벽의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="918f0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="918f0-120">-PassThru</span></span>
<span data-ttu-id="918f0-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="918f0-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="918f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="918f0-124">이 cmdlet에서 제거하는 방화벽을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="918f0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="918f0-125">-Confirm</span></span>
<span data-ttu-id="918f0-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="918f0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="918f0-127">-WhatIf</span></span>
<span data-ttu-id="918f0-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="918f0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="918f0-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="918f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918f0-130">CommonParameters</span></span>
<span data-ttu-id="918f0-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="918f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918f0-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="918f0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918f0-133">입력</span><span class="sxs-lookup"><span data-stu-id="918f0-133">INPUTS</span></span>

### <span data-ttu-id="918f0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="918f0-134">System.String</span></span>

## <span data-ttu-id="918f0-135">출력</span><span class="sxs-lookup"><span data-stu-id="918f0-135">OUTPUTS</span></span>

### <span data-ttu-id="918f0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="918f0-136">System.Boolean</span></span>

## <span data-ttu-id="918f0-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="918f0-137">NOTES</span></span>

## <span data-ttu-id="918f0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="918f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="918f0-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="918f0-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="918f0-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="918f0-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="918f0-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="918f0-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)