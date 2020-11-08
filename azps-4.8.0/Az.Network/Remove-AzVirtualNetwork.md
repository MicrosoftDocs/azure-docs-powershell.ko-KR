---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214344"
---
# <span data-ttu-id="e6043-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6043-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="e6043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6043-102">SYNOPSIS</span></span>
<span data-ttu-id="e6043-103">가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-103">Removes a virtual network.</span></span>

## <span data-ttu-id="e6043-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6043-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6043-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6043-105">DESCRIPTION</span></span>
<span data-ttu-id="e6043-106">**AzVirtualNetwork** Cmdlet은 Azure 가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="e6043-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6043-107">EXAMPLES</span></span>

### <span data-ttu-id="e6043-108">1: 가상 네트워크 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="e6043-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="e6043-109">이 예제에서는 리소스 그룹에 가상 네트워크를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e6043-110">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e6043-111">변수</span><span class="sxs-lookup"><span data-stu-id="e6043-111">PARAMETERS</span></span>

### <span data-ttu-id="e6043-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6043-112">-AsJob</span></span>
<span data-ttu-id="e6043-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6043-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6043-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6043-114">-DefaultProfile</span></span>
<span data-ttu-id="e6043-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6043-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e6043-116">-Force</span></span>
<span data-ttu-id="e6043-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6043-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e6043-118">-Name</span></span>
<span data-ttu-id="e6043-119">이 cmdlet이 제거 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6043-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6043-120">-PassThru</span></span>
<span data-ttu-id="e6043-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6043-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6043-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6043-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6043-124">이 cmdlet이 제거 하는 가상 네트워크를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6043-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e6043-125">-Confirm</span></span>
<span data-ttu-id="e6043-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6043-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6043-127">-WhatIf</span></span>
<span data-ttu-id="e6043-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6043-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6043-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6043-130">CommonParameters</span></span>
<span data-ttu-id="e6043-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6043-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6043-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6043-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6043-133">입력</span><span class="sxs-lookup"><span data-stu-id="e6043-133">INPUTS</span></span>

### <span data-ttu-id="e6043-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6043-134">System.String</span></span>

## <span data-ttu-id="e6043-135">출력</span><span class="sxs-lookup"><span data-stu-id="e6043-135">OUTPUTS</span></span>

### <span data-ttu-id="e6043-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e6043-136">System.Boolean</span></span>

## <span data-ttu-id="e6043-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e6043-137">NOTES</span></span>

## <span data-ttu-id="e6043-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6043-138">RELATED LINKS</span></span>

[<span data-ttu-id="e6043-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6043-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e6043-140">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6043-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e6043-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6043-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

