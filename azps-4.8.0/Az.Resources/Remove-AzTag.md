---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 05ee8609c7ee8bccd435e6e861f67829b9988d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204401"
---
# <span data-ttu-id="e5047-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="e5047-101">Remove-AzTag</span></span>

## <span data-ttu-id="e5047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5047-102">SYNOPSIS</span></span>
<span data-ttu-id="e5047-103">미리 정의 된 Azure 태그 또는 값을 삭제 합니다. | 리소스나 구독에 대 한 전체 태그 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="e5047-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5047-104">SYNTAX</span></span>

### <span data-ttu-id="e5047-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5047-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5047-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5047-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="e5047-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e5047-107">DESCRIPTION</span></span>

<span data-ttu-id="e5047-108">**RemovePredefinedTagSet** : **Remove-AzTag** cmdlet은 구독에서 미리 정의 된 Azure 태그 및 값을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="e5047-109">미리 정의 된 태그에서 특정 값을 삭제 하려면 *Value* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="e5047-110">기본적으로 **-AzTag** 에서는 지정 된 태그와 모든 값을 삭제 합니다. 현재 리소스나 리소스 그룹에 적용 된 태그나 값은 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="e5047-111">**Remove-AzTag** 를 사용 하기 전에 Set-AzResourceGroup Cmdlet의 *tag* 매개 변수를 사용 하 여 리소스 또는 리소스 그룹의 태그를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="e5047-112">**-AzTag를 제거** 하는 azure 태그 모듈은 미리 정의 된 azure 태그를 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="e5047-113">Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="e5047-114">한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="e5047-115">**RemoveByResourceIdParameterSet** : **ResourceId** 가 있는 **Remove-AzTag** cmdlet은 리소스나 구독에 대 한 전체 태그 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="e5047-116">예제의</span><span class="sxs-lookup"><span data-stu-id="e5047-116">EXAMPLES</span></span>

### <span data-ttu-id="e5047-117">예제 1: 미리 정의 된 태그 삭제</span><span class="sxs-lookup"><span data-stu-id="e5047-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="e5047-118">이 명령은 부서별 및 모든 값 이라는 미리 정의 된 태그를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="e5047-119">해당 태그가 리소스나 리소스 그룹에 적용 되 면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="e5047-120">예제 2: 미리 정의 된 태그에서 값 삭제</span><span class="sxs-lookup"><span data-stu-id="e5047-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="e5047-121">이 명령은 미리 정의 된 부서 태그에서 HumanResources 값을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="e5047-122">태그는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-122">It does not delete the tag.</span></span>
<span data-ttu-id="e5047-123">값이 리소스나 리소스 그룹에 적용 되 면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="e5047-124">예제 3: 구독에 대 한 전체 태그 집합 삭제</span><span class="sxs-lookup"><span data-stu-id="e5047-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="e5047-125">이 명령은 {subId}를 사용 하 여 구독에 대 한 전체 태그 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="e5047-126">"-PassThru"를 전달 하지 않으면 삭제 된 개체는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="e5047-127">예제 4: 리소스의 전체 태그 집합 삭제</span><span class="sxs-lookup"><span data-stu-id="e5047-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="e5047-128">이 명령은 {resourceId}를 사용 하 여 리소스의 전체 태그 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="e5047-129">"-PassThru"를 전달할 때 삭제 된 oject를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="e5047-130">변수</span><span class="sxs-lookup"><span data-stu-id="e5047-130">PARAMETERS</span></span>

### <span data-ttu-id="e5047-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5047-131">-DefaultProfile</span></span>
<span data-ttu-id="e5047-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5047-133">-이름</span><span class="sxs-lookup"><span data-stu-id="e5047-133">-Name</span></span>
<span data-ttu-id="e5047-134">제거할 미리 정의 된 태그의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="e5047-135">기본적으로 **AzTag 제거-** 지정 된 태그와 모든 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="e5047-136">선택한 값만 삭제 하 고 태그는 삭제 하지 않으려면 *Value* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-137">-값</span><span class="sxs-lookup"><span data-stu-id="e5047-137">-Value</span></span>
<span data-ttu-id="e5047-138">미리 정의 된 태그에서 지정 된 값을 삭제 하지만 태그를 삭제 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5047-139">-ResourceId</span></span>
<span data-ttu-id="e5047-140">태그가 지정 된 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="e5047-141">리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5047-142">-PassThru</span></span>
<span data-ttu-id="e5047-143">삭제 된 태그 또는 삭제 된 값이 있는 결과 태그를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e5047-144">-Confirm</span></span>
<span data-ttu-id="e5047-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5047-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5047-146">-WhatIf</span></span>
<span data-ttu-id="e5047-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5047-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5047-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5047-149">CommonParameters</span></span>
<span data-ttu-id="e5047-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5047-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5047-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5047-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5047-152">입력</span><span class="sxs-lookup"><span data-stu-id="e5047-152">INPUTS</span></span>

### <span data-ttu-id="e5047-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5047-153">System.String</span></span>

### <span data-ttu-id="e5047-154">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e5047-154">System.String[]</span></span>

### <span data-ttu-id="e5047-155">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5047-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5047-156">출력</span><span class="sxs-lookup"><span data-stu-id="e5047-156">OUTPUTS</span></span>

### <span data-ttu-id="e5047-157">PSTag |을 (를) 보세요. PSTagResource에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e5047-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="e5047-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e5047-158">NOTES</span></span>

## <span data-ttu-id="e5047-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5047-159">RELATED LINKS</span></span>

[<span data-ttu-id="e5047-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="e5047-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="e5047-161">새로운 AzTag</span><span class="sxs-lookup"><span data-stu-id="e5047-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="e5047-162">업데이트-AzTag</span><span class="sxs-lookup"><span data-stu-id="e5047-162">Update-AzTag</span></span>](./Update-AzTag.md)