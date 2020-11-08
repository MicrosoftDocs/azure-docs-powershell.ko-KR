---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217351"
---
# <span data-ttu-id="00667-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="00667-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="00667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00667-102">SYNOPSIS</span></span>
<span data-ttu-id="00667-103">리소스의 구성 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="00667-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00667-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00667-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00667-105">DESCRIPTION</span></span>
<span data-ttu-id="00667-106">리소스의 구성 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="00667-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00667-107">EXAMPLES</span></span>

### <span data-ttu-id="00667-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00667-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="00667-109">리소스의 구성 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="00667-110">변수</span><span class="sxs-lookup"><span data-stu-id="00667-110">PARAMETERS</span></span>

### <span data-ttu-id="00667-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00667-111">-AsJob</span></span>
<span data-ttu-id="00667-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="00667-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00667-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="00667-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="00667-114">구성 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="00667-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00667-115">-DefaultProfile</span></span>
<span data-ttu-id="00667-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00667-117">-Force</span><span class="sxs-lookup"><span data-stu-id="00667-117">-Force</span></span>
<span data-ttu-id="00667-118">확인 하지 않고 강제로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="00667-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00667-119">-PassThru</span></span>
<span data-ttu-id="00667-120">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="00667-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00667-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00667-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="00667-122">-ProviderName</span></span>
<span data-ttu-id="00667-123">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00667-124">-ResourceGroupName</span></span>
<span data-ttu-id="00667-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-126">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="00667-126">-ResourceName</span></span>
<span data-ttu-id="00667-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="00667-128">-ResourceParentName</span></span>
<span data-ttu-id="00667-129">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="00667-130">-ResourceParentType</span></span>
<span data-ttu-id="00667-131">부모 리소스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="00667-132">-ResourceType</span></span>
<span data-ttu-id="00667-133">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="00667-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00667-134">-확인</span><span class="sxs-lookup"><span data-stu-id="00667-134">-Confirm</span></span>
<span data-ttu-id="00667-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00667-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00667-136">-WhatIf</span></span>
<span data-ttu-id="00667-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00667-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00667-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00667-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00667-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00667-139">CommonParameters</span></span>
<span data-ttu-id="00667-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00667-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00667-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00667-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00667-142">입력</span><span class="sxs-lookup"><span data-stu-id="00667-142">INPUTS</span></span>

### <span data-ttu-id="00667-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00667-143">System.String</span></span>

## <span data-ttu-id="00667-144">출력</span><span class="sxs-lookup"><span data-stu-id="00667-144">OUTPUTS</span></span>

### <span data-ttu-id="00667-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="00667-145">System.Boolean</span></span>

## <span data-ttu-id="00667-146">상속자</span><span class="sxs-lookup"><span data-stu-id="00667-146">NOTES</span></span>

## <span data-ttu-id="00667-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00667-147">RELATED LINKS</span></span>