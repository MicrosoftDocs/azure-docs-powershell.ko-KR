---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047429"
---
# <span data-ttu-id="8cdf8-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdf8-101">Set-AzResource</span></span>

## <span data-ttu-id="8cdf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cdf8-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdf8-103">리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-103">Modifies a resource.</span></span>

## <span data-ttu-id="8cdf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cdf8-104">SYNTAX</span></span>

### <span data-ttu-id="8cdf8-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="8cdf8-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cdf8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cdf8-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cdf8-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8cdf8-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cdf8-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8cdf8-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cdf8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8cdf8-109">DESCRIPTION</span></span>
<span data-ttu-id="8cdf8-110">**Set-AzResource** cmdlet은 기존 Azure 리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="8cdf8-111">이름 및 형식 또는 ID를 기준으로 수정할 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="8cdf8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8cdf8-112">EXAMPLES</span></span>

### <span data-ttu-id="8cdf8-113">예제 1: 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="8cdf8-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="8cdf8-114">첫 번째 명령은 Get-AzResource cmdlet을 사용 하 여 ContosoSite 이라는 리소스를 가져온 다음 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="8cdf8-115">두 번째 명령은 $Resource의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="8cdf8-116">마지막 명령은 $Resource 일치 하도록 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="8cdf8-117">예제 2: 지정 된 리소스 그룹의 모든 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="8cdf8-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="8cdf8-118">첫 번째 명령은 testrg 리소스 그룹의 리소스를 가져온 다음이를 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="8cdf8-119">두 번째 명령은 리소스 그룹의 각 리소스에 대해 반복 하 고 새 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="8cdf8-120">마지막 명령은 이러한 각 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="8cdf8-121">변수</span><span class="sxs-lookup"><span data-stu-id="8cdf8-121">PARAMETERS</span></span>

### <span data-ttu-id="8cdf8-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cdf8-122">-ApiVersion</span></span>
<span data-ttu-id="8cdf8-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8cdf8-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8cdf8-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cdf8-125">-AsJob</span></span>
<span data-ttu-id="8cdf8-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8cdf8-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cdf8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdf8-127">-DefaultProfile</span></span>
<span data-ttu-id="8cdf8-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8cdf8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cdf8-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8cdf8-129">-ExtensionResourceName</span></span>
<span data-ttu-id="8cdf8-130">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="8cdf8-131">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="8cdf8-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8cdf8-132">-ExtensionResourceType</span></span>
<span data-ttu-id="8cdf8-133">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="8cdf8-134">예를 들어 확장 리소스가 데이터베이스인 경우 다음을 지정 합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8cdf8-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-135">-Force</span><span class="sxs-lookup"><span data-stu-id="8cdf8-135">-Force</span></span>
<span data-ttu-id="8cdf8-136">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8cdf8-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cdf8-137">-InputObject</span></span>
<span data-ttu-id="8cdf8-138">업데이트할 리소스의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-139">-종류</span><span class="sxs-lookup"><span data-stu-id="8cdf8-139">-Kind</span></span>
<span data-ttu-id="8cdf8-140">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="8cdf8-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8cdf8-141">-ODataQuery</span></span>
<span data-ttu-id="8cdf8-142">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8cdf8-143">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8cdf8-144">-계획</span><span class="sxs-lookup"><span data-stu-id="8cdf8-144">-Plan</span></span>
<span data-ttu-id="8cdf8-145">리소스에 대 한 리소스 계획 속성을 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="8cdf8-146">-Pre</span></span>
<span data-ttu-id="8cdf8-147">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8cdf8-148">-속성</span><span class="sxs-lookup"><span data-stu-id="8cdf8-148">-Properties</span></span>
<span data-ttu-id="8cdf8-149">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdf8-150">-ResourceGroupName</span></span>
<span data-ttu-id="8cdf8-151">이 cmdlet이 리소스를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cdf8-152">-ResourceId</span></span>
<span data-ttu-id="8cdf8-153">구독을 포함 하 여 정규화 된 리소스 ID를 다음 예제와 같이 지정 합니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8cdf8-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8cdf8-154">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="8cdf8-154">-ResourceName</span></span>
<span data-ttu-id="8cdf8-155">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="8cdf8-156">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8cdf8-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8cdf8-157">-ResourceType</span></span>
<span data-ttu-id="8cdf8-158">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="8cdf8-159">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8cdf8-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="8cdf8-160">-Sku</span></span>
<span data-ttu-id="8cdf8-161">리소스의 SKU 개체를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-162">태그</span><span class="sxs-lookup"><span data-stu-id="8cdf8-162">-Tag</span></span>
<span data-ttu-id="8cdf8-163">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8cdf8-164">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8cdf8-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8cdf8-165">-TenantLevel</span></span>
<span data-ttu-id="8cdf8-166">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdf8-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="8cdf8-167">-UsePatchSemantics</span></span>
<span data-ttu-id="8cdf8-168">HTTP를 사용 하지 않고이 cmdlet이 HTTP 패치를 사용 하 여 개체를 업데이트 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="8cdf8-169">-확인</span><span class="sxs-lookup"><span data-stu-id="8cdf8-169">-Confirm</span></span>
<span data-ttu-id="8cdf8-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cdf8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdf8-171">-WhatIf</span></span>
<span data-ttu-id="8cdf8-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cdf8-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cdf8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdf8-174">CommonParameters</span></span>
<span data-ttu-id="8cdf8-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdf8-176">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdf8-177">입력</span><span class="sxs-lookup"><span data-stu-id="8cdf8-177">INPUTS</span></span>

### <span data-ttu-id="8cdf8-178">SdkModels 리소스에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="8cdf8-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cdf8-179">System.String</span></span>

### <span data-ttu-id="8cdf8-180">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="8cdf8-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="8cdf8-181">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8cdf8-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8cdf8-182">출력</span><span class="sxs-lookup"><span data-stu-id="8cdf8-182">OUTPUTS</span></span>

### <span data-ttu-id="8cdf8-183">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="8cdf8-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8cdf8-184">상속자</span><span class="sxs-lookup"><span data-stu-id="8cdf8-184">NOTES</span></span>

## <span data-ttu-id="8cdf8-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cdf8-185">RELATED LINKS</span></span>

[<span data-ttu-id="8cdf8-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdf8-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="8cdf8-187">이동-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdf8-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8cdf8-188">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdf8-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8cdf8-189">제거-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdf8-189">Remove-AzResource</span></span>](./Remove-AzResource.md)