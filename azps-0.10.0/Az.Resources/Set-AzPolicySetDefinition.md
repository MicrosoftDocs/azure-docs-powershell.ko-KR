---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 21ea2a78ed14cc7fbcc343bd7905a33ef4bd126a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876361"
---
# <span data-ttu-id="ac35b-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ac35b-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ac35b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac35b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac35b-103">정책 집합 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="ac35b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac35b-104">SYNTAX</span></span>

### <span data-ttu-id="ac35b-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ac35b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac35b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac35b-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac35b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac35b-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac35b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac35b-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac35b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ac35b-109">DESCRIPTION</span></span>
<span data-ttu-id="ac35b-110">**Set-AzPolicySetDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ac35b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ac35b-111">EXAMPLES</span></span>

### <span data-ttu-id="ac35b-112">예제 1: 정책 집합 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="ac35b-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="ac35b-113">첫 번째 명령은 Get-AzPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ac35b-114">명령이 $PolicySetDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="ac35b-115">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ac35b-116">변수</span><span class="sxs-lookup"><span data-stu-id="ac35b-116">PARAMETERS</span></span>

### <span data-ttu-id="ac35b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ac35b-117">-ApiVersion</span></span>
<span data-ttu-id="ac35b-118">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ac35b-119">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ac35b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac35b-120">-DefaultProfile</span></span>
<span data-ttu-id="ac35b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ac35b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac35b-122">-설명</span><span class="sxs-lookup"><span data-stu-id="ac35b-122">-Description</span></span>
<span data-ttu-id="ac35b-123">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="ac35b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ac35b-124">-DisplayName</span></span>
<span data-ttu-id="ac35b-125">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="ac35b-126">-Id</span><span class="sxs-lookup"><span data-stu-id="ac35b-126">-Id</span></span>
<span data-ttu-id="ac35b-127">구독을 포함 하는 정규화 된 정책 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="ac35b-128">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ac35b-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac35b-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ac35b-129">-ManagementGroupName</span></span>
<span data-ttu-id="ac35b-130">업데이트할 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-130">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac35b-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ac35b-131">-Metadata</span></span>
<span data-ttu-id="ac35b-132">업데이트 된 정책 집합 정의의 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="ac35b-133">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="ac35b-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ac35b-134">-Name</span></span>
<span data-ttu-id="ac35b-135">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac35b-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ac35b-136">-Parameter</span></span>
<span data-ttu-id="ac35b-137">업데이트 된 정책 집합 정의의 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="ac35b-138">매개 변수 선언을 포함 하는 uri 또는 파일 이름에 대 한 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="ac35b-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ac35b-139">-PolicyDefinition</span></span>
<span data-ttu-id="ac35b-140">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-140">The policy set definition.</span></span> <span data-ttu-id="ac35b-141">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="ac35b-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="ac35b-142">-Pre</span></span>
<span data-ttu-id="ac35b-143">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ac35b-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac35b-144">-SubscriptionId</span></span>
<span data-ttu-id="ac35b-145">업데이트할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-145">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac35b-146">-확인</span><span class="sxs-lookup"><span data-stu-id="ac35b-146">-Confirm</span></span>
<span data-ttu-id="ac35b-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac35b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac35b-148">-WhatIf</span></span>
<span data-ttu-id="ac35b-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac35b-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac35b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac35b-151">CommonParameters</span></span>
<span data-ttu-id="ac35b-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac35b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac35b-153">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac35b-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac35b-154">입력</span><span class="sxs-lookup"><span data-stu-id="ac35b-154">INPUTS</span></span>

### <span data-ttu-id="ac35b-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac35b-155">System.String</span></span>

### <span data-ttu-id="ac35b-156">시스템 Null 허용 ' 1 [[b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="ac35b-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ac35b-157">출력</span><span class="sxs-lookup"><span data-stu-id="ac35b-157">OUTPUTS</span></span>

### <span data-ttu-id="ac35b-158">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="ac35b-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ac35b-159">상속자</span><span class="sxs-lookup"><span data-stu-id="ac35b-159">NOTES</span></span>

## <span data-ttu-id="ac35b-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac35b-160">RELATED LINKS</span></span>