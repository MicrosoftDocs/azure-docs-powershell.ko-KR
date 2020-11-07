---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2630b438fa9c5aaa691422be2da2d32e08112fba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872309"
---
# <span data-ttu-id="d3592-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d3592-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="d3592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3592-102">SYNOPSIS</span></span>
<span data-ttu-id="d3592-103">진행 중인 정책 수정 내용을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="d3592-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3592-104">SYNTAX</span></span>

### <span data-ttu-id="d3592-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3592-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3592-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3592-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3592-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3592-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3592-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d3592-108">DESCRIPTION</span></span>
<span data-ttu-id="d3592-109">**AzPolicyRemediation** cmdlet은 진행 중인 정책 수정을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="d3592-110">활성 배포가 취소 되 고 새 배포가 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="d3592-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d3592-111">EXAMPLES</span></span>

### <span data-ttu-id="d3592-112">예제 1: 리소스 그룹 범위에서 정책 업데이트 취소</span><span class="sxs-lookup"><span data-stu-id="d3592-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="d3592-113">이 명령은 리소스 그룹 ' myRG '의 ' remediation1 ' 재구성을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="d3592-114">예제 2: 파이핑을 통해 관리 그룹 재구성 취소</span><span class="sxs-lookup"><span data-stu-id="d3592-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="d3592-115">이 명령은 관리 그룹 ' mg1 '에 ' remediation1 ' 인 재구성을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="d3592-116">변수</span><span class="sxs-lookup"><span data-stu-id="d3592-116">PARAMETERS</span></span>

### <span data-ttu-id="d3592-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3592-117">-AsJob</span></span>
<span data-ttu-id="d3592-118">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d3592-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3592-119">-DefaultProfile</span></span>
<span data-ttu-id="d3592-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3592-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3592-121">-InputObject</span></span>
<span data-ttu-id="d3592-122">업데이트 관리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d3592-123">-ManagementGroupName</span></span>
<span data-ttu-id="d3592-124">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d3592-125">-Name</span></span>
<span data-ttu-id="d3592-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3592-127">-PassThru</span></span>
<span data-ttu-id="d3592-128">명령이 성공적으로 완료 되 면 True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="d3592-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3592-129">-ResourceGroupName</span></span>
<span data-ttu-id="d3592-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3592-131">-ResourceId</span></span>
<span data-ttu-id="d3592-132">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-133">-범위</span><span class="sxs-lookup"><span data-stu-id="d3592-133">-Scope</span></span>
<span data-ttu-id="d3592-134">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-134">Scope of the resource.</span></span>
<span data-ttu-id="d3592-135">즉.</span><span class="sxs-lookup"><span data-stu-id="d3592-135">E.g.</span></span>
<span data-ttu-id="d3592-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d3592-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3592-137">-확인</span><span class="sxs-lookup"><span data-stu-id="d3592-137">-Confirm</span></span>
<span data-ttu-id="d3592-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3592-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3592-139">-WhatIf</span></span>
<span data-ttu-id="d3592-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3592-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3592-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3592-142">CommonParameters</span></span>
<span data-ttu-id="d3592-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3592-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3592-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3592-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3592-145">입력</span><span class="sxs-lookup"><span data-stu-id="d3592-145">INPUTS</span></span>

### <span data-ttu-id="d3592-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3592-146">System.String</span></span>

### <span data-ttu-id="d3592-147">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d3592-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d3592-148">출력</span><span class="sxs-lookup"><span data-stu-id="d3592-148">OUTPUTS</span></span>

### <span data-ttu-id="d3592-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d3592-149">System.Boolean</span></span>

## <span data-ttu-id="d3592-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d3592-150">NOTES</span></span>

## <span data-ttu-id="d3592-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3592-151">RELATED LINKS</span></span>