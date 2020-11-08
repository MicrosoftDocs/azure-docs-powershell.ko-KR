---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215436"
---
# <span data-ttu-id="bd8f9-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="bd8f9-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="bd8f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8f9-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8f9-103">WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd8f9-103">Update WAF policy</span></span>

## <span data-ttu-id="bd8f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd8f9-104">SYNTAX</span></span>

### <span data-ttu-id="bd8f9-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bd8f9-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd8f9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd8f9-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd8f9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd8f9-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd8f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bd8f9-108">DESCRIPTION</span></span>
<span data-ttu-id="bd8f9-109">**업데이트 AzFrontDoorWafPolicy** cmdlet은 기존 waf 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="bd8f9-110">입력 매개 변수를 제공 하지 않으면 기존 WAF 정책의 이전 매개 변수가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="bd8f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bd8f9-111">EXAMPLES</span></span>

### <span data-ttu-id="bd8f9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd8f9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="bd8f9-113">기존 WAF 정책 사용자 지정 상태 코드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="bd8f9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bd8f9-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="bd8f9-115">기존 WAF 정책 모드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="bd8f9-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bd8f9-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="bd8f9-117">기존 WAF 정책 사용 상태 및 모드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="bd8f9-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="bd8f9-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="bd8f9-119">$resourceGroupName의 모든 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd8f9-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="bd8f9-120">변수</span><span class="sxs-lookup"><span data-stu-id="bd8f9-120">PARAMETERS</span></span>

### <span data-ttu-id="bd8f9-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="bd8f9-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="bd8f9-122">사용자 지정 응답 본문</span><span class="sxs-lookup"><span data-stu-id="bd8f9-122">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="bd8f9-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="bd8f9-124">사용자 지정 응답 상태 코드</span><span class="sxs-lookup"><span data-stu-id="bd8f9-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="bd8f9-125">-Customrule</span></span>
<span data-ttu-id="bd8f9-126">정책 내의 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="bd8f9-126">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8f9-127">-DefaultProfile</span></span>
<span data-ttu-id="bd8f9-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8f9-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="bd8f9-129">-EnabledState</span></span>
<span data-ttu-id="bd8f9-130">정책이 사용 상태로 설정 되어 있는지 또는 사용 안 함 상태 인지 여부</span><span class="sxs-lookup"><span data-stu-id="bd8f9-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="bd8f9-131">사용할 수 있는 값은 다음과 같습니다. ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="bd8f9-131">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd8f9-132">-InputObject</span></span>
<span data-ttu-id="bd8f9-133">업데이트할 FireWallPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="bd8f9-134">-ManagedRule</span></span>
<span data-ttu-id="bd8f9-135">정책 내 관리 규칙</span><span class="sxs-lookup"><span data-stu-id="bd8f9-135">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-136">-모드</span><span class="sxs-lookup"><span data-stu-id="bd8f9-136">-Mode</span></span>
<span data-ttu-id="bd8f9-137">정책 수준의 검색 모드 또는 방지 모드에 있는 경우에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="bd8f9-138">사용할 수 있는 값은 다음과 같습니다. ' 예방 ', ' 감지 '</span><span class="sxs-lookup"><span data-stu-id="bd8f9-138">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-139">-이름</span><span class="sxs-lookup"><span data-stu-id="bd8f9-139">-Name</span></span>
<span data-ttu-id="bd8f9-140">업데이트할 FireWallPolicy의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-141">로 RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="bd8f9-141">-RedirectUrl</span></span>
<span data-ttu-id="bd8f9-142">리디렉션 URL</span><span class="sxs-lookup"><span data-stu-id="bd8f9-142">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8f9-143">-ResourceGroupName</span></span>
<span data-ttu-id="bd8f9-144">FireWallPolicy 속해 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-144">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd8f9-145">-ResourceId</span></span>
<span data-ttu-id="bd8f9-146">업데이트할 FireWallPolicy의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f9-147">-확인</span><span class="sxs-lookup"><span data-stu-id="bd8f9-147">-Confirm</span></span>
<span data-ttu-id="bd8f9-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd8f9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd8f9-149">-WhatIf</span></span>
<span data-ttu-id="bd8f9-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd8f9-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd8f9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8f9-152">CommonParameters</span></span>
<span data-ttu-id="bd8f9-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8f9-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8f9-155">입력</span><span class="sxs-lookup"><span data-stu-id="bd8f9-155">INPUTS</span></span>

### <span data-ttu-id="bd8f9-156">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="bd8f9-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bd8f9-157">System.String</span></span>

## <span data-ttu-id="bd8f9-158">출력</span><span class="sxs-lookup"><span data-stu-id="bd8f9-158">OUTPUTS</span></span>

### <span data-ttu-id="bd8f9-159">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="bd8f9-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="bd8f9-160">상속자</span><span class="sxs-lookup"><span data-stu-id="bd8f9-160">NOTES</span></span>

## <span data-ttu-id="bd8f9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd8f9-161">RELATED LINKS</span></span>

<span data-ttu-id="bd8f9-162">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [새로운 AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [새로운 AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="bd8f9-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>