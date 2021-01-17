---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334898"
---
# <span data-ttu-id="2c99c-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2c99c-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="2c99c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c99c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c99c-103">네트워크 가상 어플라이언스 리소스에서 가상 어플라이언스 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2c99c-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c99c-104">SYNTAX</span></span>

### <span data-ttu-id="2c99c-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2c99c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c99c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c99c-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c99c-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c99c-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c99c-108">설명</span><span class="sxs-lookup"><span data-stu-id="2c99c-108">DESCRIPTION</span></span>
<span data-ttu-id="2c99c-109">Remove-AzVirtualApplianceSite 명령은 네트워크 가상 어플라이언스 리소스에서 가상 어플라이언스 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2c99c-110">예제</span><span class="sxs-lookup"><span data-stu-id="2c99c-110">EXAMPLES</span></span>

### <span data-ttu-id="2c99c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c99c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="2c99c-112">가상 어플라이언스 사이트 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="2c99c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c99c-113">PARAMETERS</span></span>

### <span data-ttu-id="2c99c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c99c-114">-AsJob</span></span>
<span data-ttu-id="2c99c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2c99c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c99c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c99c-116">-DefaultProfile</span></span>
<span data-ttu-id="2c99c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c99c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2c99c-118">-Force</span></span>
<span data-ttu-id="2c99c-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c99c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2c99c-120">-Name</span></span>
<span data-ttu-id="2c99c-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c99c-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="2c99c-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="2c99c-123">이 사이트와 연결된 네트워크 가상 어플라이언스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c99c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c99c-124">-PassThru</span></span>
<span data-ttu-id="2c99c-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2c99c-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c99c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c99c-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c99c-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c99c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c99c-129">-ResourceId</span></span>
<span data-ttu-id="2c99c-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c99c-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2c99c-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="2c99c-132">가상 어플라이언스 사이트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c99c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c99c-133">-Confirm</span></span>
<span data-ttu-id="2c99c-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c99c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c99c-135">-WhatIf</span></span>
<span data-ttu-id="2c99c-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c99c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c99c-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c99c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c99c-138">CommonParameters</span></span>
<span data-ttu-id="2c99c-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c99c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c99c-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c99c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c99c-141">입력</span><span class="sxs-lookup"><span data-stu-id="2c99c-141">INPUTS</span></span>

### <span data-ttu-id="2c99c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2c99c-142">System.String</span></span>

### <span data-ttu-id="2c99c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2c99c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="2c99c-144">출력</span><span class="sxs-lookup"><span data-stu-id="2c99c-144">OUTPUTS</span></span>

### <span data-ttu-id="2c99c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c99c-145">System.Boolean</span></span>

## <span data-ttu-id="2c99c-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c99c-146">NOTES</span></span>

## <span data-ttu-id="2c99c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c99c-147">RELATED LINKS</span></span>