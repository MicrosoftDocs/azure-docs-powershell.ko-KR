---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370917"
---
# <span data-ttu-id="58215-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="58215-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="58215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58215-102">SYNOPSIS</span></span>
<span data-ttu-id="58215-103">네트워크 인터페이스에 대한 탭 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="58215-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="58215-104">구문</span><span class="sxs-lookup"><span data-stu-id="58215-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58215-105">설명</span><span class="sxs-lookup"><span data-stu-id="58215-105">DESCRIPTION</span></span>
<span data-ttu-id="58215-106">**Set-AzNetworkInterfaceTapConfig는** 네트워크 인터페이스에 대한 탭 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="58215-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="58215-107">예제</span><span class="sxs-lookup"><span data-stu-id="58215-107">EXAMPLES</span></span>

### <span data-ttu-id="58215-108">예제 1: 업데이트된 TapConfig 이름으로 TapConfiguration 설정</span><span class="sxs-lookup"><span data-stu-id="58215-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="58215-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58215-109">PARAMETERS</span></span>

### <span data-ttu-id="58215-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58215-110">-AsJob</span></span>
<span data-ttu-id="58215-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="58215-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58215-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58215-112">-DefaultProfile</span></span>
<span data-ttu-id="58215-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58215-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58215-114">-Force</span><span class="sxs-lookup"><span data-stu-id="58215-114">-Force</span></span>
<span data-ttu-id="58215-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58215-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="58215-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="58215-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="58215-117">NetworkInterface Tap 구성</span><span class="sxs-lookup"><span data-stu-id="58215-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58215-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58215-118">-Confirm</span></span>
<span data-ttu-id="58215-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="58215-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58215-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58215-120">-WhatIf</span></span>
<span data-ttu-id="58215-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="58215-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58215-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58215-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58215-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58215-123">CommonParameters</span></span>
<span data-ttu-id="58215-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58215-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58215-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="58215-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58215-126">입력</span><span class="sxs-lookup"><span data-stu-id="58215-126">INPUTS</span></span>

### <span data-ttu-id="58215-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="58215-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="58215-128">출력</span><span class="sxs-lookup"><span data-stu-id="58215-128">OUTPUTS</span></span>

### <span data-ttu-id="58215-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="58215-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="58215-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58215-130">NOTES</span></span>

## <span data-ttu-id="58215-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58215-131">RELATED LINKS</span></span>

[<span data-ttu-id="58215-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="58215-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="58215-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="58215-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="58215-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="58215-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)