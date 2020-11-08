---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ecd70916f1ddb6e365fb9f880db9974f6c9ae771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204408"
---
# <span data-ttu-id="d6748-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-101">Remove-AzResource</span></span>

## <span data-ttu-id="d6748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6748-102">SYNOPSIS</span></span>
<span data-ttu-id="d6748-103">리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-103">Removes a resource.</span></span>

## <span data-ttu-id="d6748-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6748-104">SYNTAX</span></span>

### <span data-ttu-id="d6748-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6748-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6748-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d6748-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6748-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d6748-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6748-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6748-108">DESCRIPTION</span></span>
<span data-ttu-id="d6748-109">**AzResource** Cmdlet은 Azure 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="d6748-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6748-110">EXAMPLES</span></span>

### <span data-ttu-id="d6748-111">예제 1: 웹 사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="d6748-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="d6748-112">이 명령은 ContosoSite 이라는 웹 사이트 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="d6748-113">이 예제에서는 구독 ID에 대 한 자리 표시자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="d6748-114">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d6748-115">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d6748-116">변수</span><span class="sxs-lookup"><span data-stu-id="d6748-116">PARAMETERS</span></span>

### <span data-ttu-id="d6748-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6748-117">-ApiVersion</span></span>
<span data-ttu-id="d6748-118">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6748-119">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d6748-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6748-120">-AsJob</span></span>
<span data-ttu-id="d6748-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d6748-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6748-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6748-122">-DefaultProfile</span></span>
<span data-ttu-id="d6748-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6748-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6748-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d6748-124">-ExtensionResourceName</span></span>
<span data-ttu-id="d6748-125">이 cmdlet이 제거 하는 리소스의 확장 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="d6748-126">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="d6748-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="d6748-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d6748-127">-ExtensionResourceType</span></span>
<span data-ttu-id="d6748-128">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="d6748-129">자원에 대 한 확장 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="d6748-130">예를 들면 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="d6748-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="d6748-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d6748-131">-Force</span></span>
<span data-ttu-id="d6748-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6748-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d6748-133">-ODataQuery</span></span>
<span data-ttu-id="d6748-134">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="d6748-135">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="d6748-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6748-136">-Pre</span></span>
<span data-ttu-id="d6748-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d6748-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6748-138">-ResourceGroupName</span></span>
<span data-ttu-id="d6748-139">이 cmdlet이 리소스를 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="d6748-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6748-140">-ResourceId</span></span>
<span data-ttu-id="d6748-141">이 cmdlet이 제거 하는 리소스의 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="d6748-142">ID에는 다음 예제와 같이 구독이 포함 됩니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d6748-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="d6748-143">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="d6748-143">-ResourceName</span></span>
<span data-ttu-id="d6748-144">이 cmdlet이 제거 하는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="d6748-145">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d6748-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="d6748-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d6748-146">-ResourceType</span></span>
<span data-ttu-id="d6748-147">이 cmdlet이 제거 하는 리소스의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="d6748-148">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="d6748-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="d6748-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d6748-149">-TenantLevel</span></span>
<span data-ttu-id="d6748-150">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="d6748-151">-확인</span><span class="sxs-lookup"><span data-stu-id="d6748-151">-Confirm</span></span>
<span data-ttu-id="d6748-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6748-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6748-153">-WhatIf</span></span>
<span data-ttu-id="d6748-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6748-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6748-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6748-156">CommonParameters</span></span>
<span data-ttu-id="d6748-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6748-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6748-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6748-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6748-159">입력</span><span class="sxs-lookup"><span data-stu-id="d6748-159">INPUTS</span></span>

### <span data-ttu-id="d6748-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6748-160">System.String</span></span>

## <span data-ttu-id="d6748-161">출력</span><span class="sxs-lookup"><span data-stu-id="d6748-161">OUTPUTS</span></span>

### <span data-ttu-id="d6748-162">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d6748-162">System.Boolean</span></span>

## <span data-ttu-id="d6748-163">상속자</span><span class="sxs-lookup"><span data-stu-id="d6748-163">NOTES</span></span>

## <span data-ttu-id="d6748-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6748-164">RELATED LINKS</span></span>

[<span data-ttu-id="d6748-165">찾기-AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-165">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="d6748-166">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-166">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="d6748-167">이동-AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-167">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="d6748-168">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-168">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="d6748-169">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="d6748-169">Set-AzResource</span></span>](./Set-AzResource.md)

