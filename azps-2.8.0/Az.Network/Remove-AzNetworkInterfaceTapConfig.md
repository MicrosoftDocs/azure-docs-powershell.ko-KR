---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 8ad89a0f5fad61fea2ba898ea17f63b6f935ae84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871213"
---
# <span data-ttu-id="78f76-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="78f76-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="78f76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f76-102">SYNOPSIS</span></span>
<span data-ttu-id="78f76-103">지정 된 네트워크 인터페이스에서 탭 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="78f76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78f76-104">SYNTAX</span></span>

### <span data-ttu-id="78f76-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="78f76-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f76-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f76-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f76-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f76-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f76-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78f76-108">DESCRIPTION</span></span>
<span data-ttu-id="78f76-109">**AzNetworkInterfaceTapConfig** cmdlet은 네트워크 인터페이스 목록에서 Azure 탭 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="78f76-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78f76-110">EXAMPLES</span></span>

### <span data-ttu-id="78f76-111">예제 1: 탭 구성 제거</span><span class="sxs-lookup"><span data-stu-id="78f76-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="78f76-112">이 명령은 리소스 그룹 ResourceGroup1의 NetworkInterface1에서 TapConfiguration를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="78f76-113">*Force* 매개 변수는 사용 되지 않으므로 사용자에 게이 작업을 확인 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="78f76-114">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="78f76-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="78f76-115">이 명령은 리소스 그룹 ResourceGroup1의 NetworkInterface1에서 TapConfiguration를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="78f76-116">*Force* 매개 변수를 사용 하기 때문에 사용자에 게 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="78f76-117">변수</span><span class="sxs-lookup"><span data-stu-id="78f76-117">PARAMETERS</span></span>

### <span data-ttu-id="78f76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f76-118">-DefaultProfile</span></span>
<span data-ttu-id="78f76-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f76-120">-Force</span><span class="sxs-lookup"><span data-stu-id="78f76-120">-Force</span></span>
<span data-ttu-id="78f76-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="78f76-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f76-122">-InputObject</span></span>
<span data-ttu-id="78f76-123">NetworkInterfaceTapConfig에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f76-124">-이름</span><span class="sxs-lookup"><span data-stu-id="78f76-124">-Name</span></span>
<span data-ttu-id="78f76-125">가상 네트워크 피어 링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f76-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="78f76-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="78f76-127">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f76-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78f76-128">-PassThru</span></span>
<span data-ttu-id="78f76-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78f76-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78f76-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f76-131">-ResourceGroupName</span></span>
<span data-ttu-id="78f76-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f76-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78f76-133">-ResourceId</span></span>
<span data-ttu-id="78f76-134">NetworkInterfaceTapConfig 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f76-135">-확인</span><span class="sxs-lookup"><span data-stu-id="78f76-135">-Confirm</span></span>
<span data-ttu-id="78f76-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f76-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f76-137">-WhatIf</span></span>
<span data-ttu-id="78f76-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f76-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f76-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f76-140">CommonParameters</span></span>
<span data-ttu-id="78f76-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f76-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f76-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f76-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f76-143">입력</span><span class="sxs-lookup"><span data-stu-id="78f76-143">INPUTS</span></span>

### <span data-ttu-id="78f76-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78f76-144">System.String</span></span>

### <span data-ttu-id="78f76-145">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="78f76-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="78f76-146">출력</span><span class="sxs-lookup"><span data-stu-id="78f76-146">OUTPUTS</span></span>

### <span data-ttu-id="78f76-147">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="78f76-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="78f76-148">상속자</span><span class="sxs-lookup"><span data-stu-id="78f76-148">NOTES</span></span>

## <span data-ttu-id="78f76-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78f76-149">RELATED LINKS</span></span>

[<span data-ttu-id="78f76-150">추가-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="78f76-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="78f76-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="78f76-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="78f76-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="78f76-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)