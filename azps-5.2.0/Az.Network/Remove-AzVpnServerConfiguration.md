---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345873"
---
# <span data-ttu-id="02105-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="02105-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="02105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02105-102">SYNOPSIS</span></span>
<span data-ttu-id="02105-103">기존 VpnServerConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02105-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="02105-104">구문</span><span class="sxs-lookup"><span data-stu-id="02105-104">SYNTAX</span></span>

### <span data-ttu-id="02105-105">ByVpnServerConfigurationName(기본값)</span><span class="sxs-lookup"><span data-stu-id="02105-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02105-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="02105-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02105-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="02105-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02105-108">설명</span><span class="sxs-lookup"><span data-stu-id="02105-108">DESCRIPTION</span></span>
<span data-ttu-id="02105-109">{{설명 입력}}</span><span class="sxs-lookup"><span data-stu-id="02105-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="02105-110">예제</span><span class="sxs-lookup"><span data-stu-id="02105-110">EXAMPLES</span></span>

### <span data-ttu-id="02105-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="02105-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="02105-112">위의 명령은 기존 VpnServerConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02105-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="02105-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02105-113">PARAMETERS</span></span>

### <span data-ttu-id="02105-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02105-114">-DefaultProfile</span></span>
<span data-ttu-id="02105-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02105-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02105-116">-Force</span><span class="sxs-lookup"><span data-stu-id="02105-116">-Force</span></span>
<span data-ttu-id="02105-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02105-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02105-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02105-118">-InputObject</span></span>
<span data-ttu-id="02105-119">삭제할 vpnServerConfiguration 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02105-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02105-120">-Name</span><span class="sxs-lookup"><span data-stu-id="02105-120">-Name</span></span>
<span data-ttu-id="02105-121">vpnServerConfiguration 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02105-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02105-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02105-122">-PassThru</span></span>
<span data-ttu-id="02105-123">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="02105-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="02105-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02105-124">-ResourceGroupName</span></span>
<span data-ttu-id="02105-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02105-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02105-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02105-126">-ResourceId</span></span>
<span data-ttu-id="02105-127">삭제할 vpnServerConfiguration에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02105-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02105-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02105-128">-Confirm</span></span>
<span data-ttu-id="02105-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02105-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02105-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02105-130">-WhatIf</span></span>
<span data-ttu-id="02105-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="02105-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02105-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02105-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02105-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02105-133">CommonParameters</span></span>
<span data-ttu-id="02105-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02105-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02105-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="02105-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02105-136">입력</span><span class="sxs-lookup"><span data-stu-id="02105-136">INPUTS</span></span>

### <span data-ttu-id="02105-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="02105-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="02105-138">System.String</span><span class="sxs-lookup"><span data-stu-id="02105-138">System.String</span></span>

## <span data-ttu-id="02105-139">출력</span><span class="sxs-lookup"><span data-stu-id="02105-139">OUTPUTS</span></span>

### <span data-ttu-id="02105-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02105-140">System.Boolean</span></span>

## <span data-ttu-id="02105-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02105-141">NOTES</span></span>

## <span data-ttu-id="02105-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02105-142">RELATED LINKS</span></span>