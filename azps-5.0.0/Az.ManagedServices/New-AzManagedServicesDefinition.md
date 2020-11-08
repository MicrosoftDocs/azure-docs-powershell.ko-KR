---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217335"
---
# <span data-ttu-id="e6f83-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e6f83-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="e6f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f83-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f83-103">등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="e6f83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6f83-104">SYNTAX</span></span>

### <span data-ttu-id="e6f83-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6f83-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f83-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="e6f83-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f83-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="e6f83-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f83-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e6f83-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f83-109">등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="e6f83-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e6f83-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f83-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6f83-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="e6f83-112">직접 주어진 roleDefinitionId 및 principalId 값을 기준으로 등록 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="e6f83-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e6f83-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="e6f83-114">인증 세부 정보를 사용 하 여 등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="e6f83-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e6f83-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="e6f83-116">인증 세부 정보 및 등록 정의의 이름을 사용 하 여 등록 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="e6f83-117">변수</span><span class="sxs-lookup"><span data-stu-id="e6f83-117">PARAMETERS</span></span>

### <span data-ttu-id="e6f83-118">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="e6f83-118">-Authorization</span></span>
<span data-ttu-id="e6f83-119">PrincipalId-roleDefinitionId 인 인증 매핑 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f83-120">-DefaultProfile</span></span>
<span data-ttu-id="e6f83-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f83-122">-설명</span><span class="sxs-lookup"><span data-stu-id="e6f83-122">-Description</span></span>
<span data-ttu-id="e6f83-123">등록 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="e6f83-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e6f83-124">-DisplayName</span></span>
<span data-ttu-id="e6f83-125">등록 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="e6f83-126">-ManagedByTenantId</span></span>
<span data-ttu-id="e6f83-127">ManagedBy 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-128">-이름</span><span class="sxs-lookup"><span data-stu-id="e6f83-128">-Name</span></span>
<span data-ttu-id="e6f83-129">등록 정의의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="e6f83-130">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="e6f83-130">-PlanName</span></span>
<span data-ttu-id="e6f83-131">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-132">계획 제품</span><span class="sxs-lookup"><span data-stu-id="e6f83-132">-PlanProduct</span></span>
<span data-ttu-id="e6f83-133">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-134">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="e6f83-134">-PlanPublisher</span></span>
<span data-ttu-id="e6f83-135">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-136">-계획 버전</span><span class="sxs-lookup"><span data-stu-id="e6f83-136">-PlanVersion</span></span>
<span data-ttu-id="e6f83-137">계획의 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="e6f83-138">-PrincipalId</span></span>
<span data-ttu-id="e6f83-139">ManagedBy Principal 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e6f83-140">-RoleDefinitionId</span></span>
<span data-ttu-id="e6f83-141">보안 주체 식별자에 권한을 부여할 역할 정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f83-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6f83-142">-AsJob</span></span>
<span data-ttu-id="e6f83-143">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6f83-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6f83-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e6f83-144">-Confirm</span></span>
<span data-ttu-id="e6f83-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f83-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f83-146">-WhatIf</span></span>
<span data-ttu-id="e6f83-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f83-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f83-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f83-149">CommonParameters</span></span>
<span data-ttu-id="e6f83-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f83-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f83-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6f83-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f83-152">입력</span><span class="sxs-lookup"><span data-stu-id="e6f83-152">INPUTS</span></span>

### <span data-ttu-id="e6f83-153">않아야</span><span class="sxs-lookup"><span data-stu-id="e6f83-153">None</span></span>
## <span data-ttu-id="e6f83-154">출력</span><span class="sxs-lookup"><span data-stu-id="e6f83-154">OUTPUTS</span></span>

### <span data-ttu-id="e6f83-155">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="e6f83-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="e6f83-156">상속자</span><span class="sxs-lookup"><span data-stu-id="e6f83-156">NOTES</span></span>

## <span data-ttu-id="e6f83-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6f83-157">RELATED LINKS</span></span>