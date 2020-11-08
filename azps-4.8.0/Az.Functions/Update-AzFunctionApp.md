---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056354"
---
# <span data-ttu-id="7905b-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="7905b-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="7905b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7905b-102">SYNOPSIS</span></span>
<span data-ttu-id="7905b-103">함수 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-103">Updates a function app.</span></span>

## <span data-ttu-id="7905b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7905b-104">SYNTAX</span></span>

### <span data-ttu-id="7905b-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7905b-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7905b-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="7905b-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7905b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7905b-107">DESCRIPTION</span></span>
<span data-ttu-id="7905b-108">함수 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-108">Updates a function app.</span></span>

## <span data-ttu-id="7905b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7905b-109">EXAMPLES</span></span>

### <span data-ttu-id="7905b-110">예제 1: Update 함수 앱 호스팅 계획</span><span class="sxs-lookup"><span data-stu-id="7905b-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="7905b-111">이 명령은 함수 앱 호스팅 계획을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="7905b-112">예제 2: 기능 앱에 대해 SystemAssigned 된 관리 되는 id 설정</span><span class="sxs-lookup"><span data-stu-id="7905b-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="7905b-113">이 명령은 SystemAssigned 함수 앱에 대해 관리 되는 id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="7905b-114">예제 3: Update 함수 앱 Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7905b-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="7905b-115">이 명령은 함수 앱 Application Insights를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="7905b-116">예제 3: 함수 앱에서 관리 되는 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="7905b-117">이 명령은 함수 앱에서 관리 되는 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="7905b-118">변수</span><span class="sxs-lookup"><span data-stu-id="7905b-118">PARAMETERS</span></span>

### <span data-ttu-id="7905b-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="7905b-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="7905b-120">추가할 앱 Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="7905b-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="7905b-122">함수 앱에 추가할 기존 App Insights 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7905b-123">-AsJob</span></span>
<span data-ttu-id="7905b-124">백그라운드 작업으로 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="7905b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7905b-125">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="7905b-126">-IdentityID</span></span>
<span data-ttu-id="7905b-127">함수 앱과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="7905b-128">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7905b-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7905b-129">-IdentityType</span></span>
<span data-ttu-id="7905b-130">함수 앱에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="7905b-131">' 없음 ' 형식은 함수 앱에서 모든 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="7905b-132">이 매개 변수에 허용 되는 값은-SystemAssigned 됨-UserAssigned 됨입니다. 없음</span><span class="sxs-lookup"><span data-stu-id="7905b-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7905b-133">-InputObject</span></span>
<span data-ttu-id="7905b-134">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-135">-이름</span><span class="sxs-lookup"><span data-stu-id="7905b-135">-Name</span></span>
<span data-ttu-id="7905b-136">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-136">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7905b-137">-NoWait</span></span>
<span data-ttu-id="7905b-138">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="7905b-139">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7905b-140">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="7905b-140">-PlanName</span></span>
<span data-ttu-id="7905b-141">서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="7905b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7905b-142">-ResourceGroupName</span></span>
<span data-ttu-id="7905b-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7905b-144">-SubscriptionId</span></span>
<span data-ttu-id="7905b-145">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-145">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-146">태그</span><span class="sxs-lookup"><span data-stu-id="7905b-146">-Tag</span></span>
<span data-ttu-id="7905b-147">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="7905b-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7905b-148">-확인</span><span class="sxs-lookup"><span data-stu-id="7905b-148">-Confirm</span></span>
<span data-ttu-id="7905b-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7905b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7905b-150">-WhatIf</span></span>
<span data-ttu-id="7905b-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7905b-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7905b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7905b-153">CommonParameters</span></span>
<span data-ttu-id="7905b-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7905b-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7905b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7905b-156">입력</span><span class="sxs-lookup"><span data-stu-id="7905b-156">INPUTS</span></span>

### <span data-ttu-id="7905b-157">Api20190801. ISite의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="7905b-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="7905b-158">출력</span><span class="sxs-lookup"><span data-stu-id="7905b-158">OUTPUTS</span></span>

### <span data-ttu-id="7905b-159">Api20190801. ISite의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="7905b-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="7905b-160">상속자</span><span class="sxs-lookup"><span data-stu-id="7905b-160">NOTES</span></span>

<span data-ttu-id="7905b-161">별칭과</span><span class="sxs-lookup"><span data-stu-id="7905b-161">ALIASES</span></span>

<span data-ttu-id="7905b-162">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7905b-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7905b-163">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7905b-164">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7905b-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7905b-165">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="7905b-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="7905b-166">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="7905b-167">`CloningInfoSourceWebAppId <String>`: ARM 원본 앱의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="7905b-168">앱 리소스 ID는 프로덕션 슬롯 및 다른 슬롯의/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}에 대 한/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="7905b-169">`[Kind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="7905b-170">`[Tag <IResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="7905b-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="7905b-171">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7905b-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> <code>false</code> 동일한 세션에서 클라이언트 요청을 동일한 인스턴스로 라우팅하기 위해 클라이언트 선호도를 사용 하도록 설정 하 고 세션 선호도 쿠키 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="7905b-173">기본값은 <code>true</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="7905b-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증 (TLS 상호 인증)을 사용 하도록 설정 하는 방법, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="7905b-175">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-176">`[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 쉼표로 구분 된 제외 경로</span><span class="sxs-lookup"><span data-stu-id="7905b-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="7905b-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제 된 앱에 대 한 응용 프로그램 설정 재정의입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="7905b-178">이 설정을 지정 하면 원본 앱에서 복제 된 설정이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="7905b-179">그렇지 않으면 원본 앱의 응용 프로그램 설정이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="7905b-180">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7905b-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> 원본 앱에서 사용자 지정 호스트 이름을 복제 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> 원본 앱에서 원본 컨트롤을 복제 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> 원본 및 대상 앱에 대 한 부하 분산을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="7905b-184">`[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="7905b-185">이 ID는 여러 복제 작업을 결합 하 여 동일한 스냅숏을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="7905b-186">`[CloningInfoHostingEnvironment <String>]`: 앱 서비스 환경.</span><span class="sxs-lookup"><span data-stu-id="7905b-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="7905b-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어쓰려면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-188">`[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서 부 또는 서유럽</span><span class="sxs-lookup"><span data-stu-id="7905b-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="7905b-189">`[CloningInfoTrafficManagerProfileId <String>]`: 사용할 Traffic Manager 프로필의 ARM 리소스 ID입니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="7905b-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="7905b-190">Traffic Manager 리소스 ID의 형식/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="7905b-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="7905b-191">`[CloningInfoTrafficManagerProfileName <String>]`: 만들려는 Traffic Manager 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="7905b-192">이는 Traffic Manager 프로필이 아직 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="7905b-193">`[Config <ISiteConfig>]`: 앱의 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="7905b-194">`IsPushEnabled <Boolean>`: 푸시 끝점을 사용할 수 있는지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="7905b-195">`[ActionMinProcessExecutionTime <String>]`: 작업을 수행 하기 전에 프로세스를 실행 해야 하는 최소 시간</span><span class="sxs-lookup"><span data-stu-id="7905b-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="7905b-196">`[ActionType <AutoHealActionType?>]`: 수행 되도록 미리 정의 된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="7905b-197">`[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용 하도록 설정 되 면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-198">`[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="7905b-199">`[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="7905b-200">`[AppCommandLine <String>]`: 실행할 앱 명령줄입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="7905b-201">`[AppSetting <INameValuePair[]>]`: 응용 프로그램 설정</span><span class="sxs-lookup"><span data-stu-id="7905b-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="7905b-202">`[Name <String>]`: 쌍 이름.</span><span class="sxs-lookup"><span data-stu-id="7905b-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="7905b-203">`[Value <String>]`: Pair 값.</span><span class="sxs-lookup"><span data-stu-id="7905b-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="7905b-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> 자동 치료를 사용 하는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-205">`[AutoSwapSlotName <String>]`: 자동 스왑 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="7905b-206">`[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="7905b-207">`[ConnectionString <String>]`: 연결 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="7905b-208">`[Name <String>]`: 연결 문자열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="7905b-209">`[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="7905b-210">`[CorAllowedOrigin <String[]>]`: 교차 원본 호출을 허용 해야 하는 원본 목록 (예:)을 가져오거나 설정 http://example.com:12345) 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="7905b-211">"\*"를 사용 하 여 all을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="7905b-212">`[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용 하 여 CORS 요청을 사용할 수 있는지 여부를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="7905b-213">자세한 내용은         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7905b-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="7905b-214">`[CustomActionExe <String>]`: 실행할 실행 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="7905b-215">`[CustomActionParameter <String>]`: 실행 파일에 대 한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="7905b-216">`[DefaultDocument <String[]>]`: 기본 문서.</span><span class="sxs-lookup"><span data-stu-id="7905b-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="7905b-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅이 사용 되는 경우, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-218">`[DocumentRoot <String>]`: 문서 루트</span><span class="sxs-lookup"><span data-stu-id="7905b-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="7905b-219">`[DynamicTagsJson <String>]`: 푸시 등록 끝점의 사용자 클레임에서 평가 되는 동적 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="7905b-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: 램프 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="7905b-221">`[ActionHostName <String>]`: 트래픽을 결정 하는 경우 트래픽이 리디렉션되는 슬롯의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="7905b-222">즉.</span><span class="sxs-lookup"><span data-stu-id="7905b-222">E.g.</span></span> <span data-ttu-id="7905b-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="7905b-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="7905b-224">`[ChangeDecisionCallbackUrl <String>]`: 사용자 지정 결정 알고리즘은 TiPCallback 사이트 확장에서 지정할 수 있는 URL을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="7905b-225">모델링 및 계약에 대 한 TiPCallback 사이트 확장을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7905b-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="7905b-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="7905b-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="7905b-227">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 계산 하는 간격 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="7905b-228">`[ChangeStep <Double?>]`: 자동 램프 시나리오에서 <code>ReroutePercentage</code> \n 또는에 도달할 때까지 추가/제거 하는 단계입니다 <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="7905b-229">사이트 메트릭은 .\NCustom 의사 결정 알고리즘에 지정 된 매 N 분을 <code>ChangeIntervalInMinutes</code> TiPCallback site extension에서 제공 하 고 URL에서 지정할 수 있는 것으로 확인 됩니다 <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="7905b-230">`[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지 되는 위쪽 경계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="7905b-231">`[MinReroutePercentage <Double?>]`: ReroutePercentage이 유지 되는 아래쪽 경계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="7905b-232">`[Name <String>]`: 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="7905b-233">권장 되는 이름은 실험에서 트래픽을 수신 하는 슬롯을 가리키도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="7905b-234">`[ReroutePercentage <Double?>]`: 리디렉션되는 소통량의 백분율 <code>ActionHostName</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="7905b-235">`[FtpsState <FtpsState?>]`: FTP/FTPS 서비스의 상태</span><span class="sxs-lookup"><span data-stu-id="7905b-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="7905b-236">`[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑.</span><span class="sxs-lookup"><span data-stu-id="7905b-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="7905b-237">`[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="7905b-238">`[Extension <String>]`:이 확장명을 가진 요청은 지정 된 FastCGI 응용 프로그램을 사용 하 여 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="7905b-239">`[ScriptProcessor <String>]`: FastCGI 응용 프로그램의 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="7905b-240">`[HealthCheckPath <String>]`: 상태 검사 경로</span><span class="sxs-lookup"><span data-stu-id="7905b-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="7905b-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http 2.0을 통해 연결할 수 있도록 웹 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="7905b-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅이 사용 하도록 설정 되어 있으면 이 고, 그렇지 않으면 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: 메인에 대 한 IP 보안 제한.</span><span class="sxs-lookup"><span data-stu-id="7905b-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="7905b-244">`[Action <String>]`:이 IP 범위에 대 한 액세스를 허용 하거나 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="7905b-245">`[Description <String>]`: IP 제한 규칙 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="7905b-246">`[IPAddress <String>]`: IP 주소 보안 제한이에 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="7905b-247">순수한 ipv4 주소 (필수 SubnetMask 속성) 또는 ipv4/ipv6 표기법 (예: ipv4/mask (행간 비트 일치))의 형태가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="7905b-248">CIDR의 경우 SubnetMask 속성을 지정 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="7905b-249">`[Name <String>]`: IP 제한 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="7905b-250">`[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="7905b-251">`[SubnetMask <String>]`: 제한이 유효한 IP 주소 범위에 대 한 서브넷 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="7905b-252">`[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="7905b-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="7905b-253">`[Tag <IPFilterTag?>]`:이 IP 필터를 사용할 용도를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="7905b-254">이는 프록시에서 IP 필터링을 지원 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="7905b-255">`[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 id</span><span class="sxs-lookup"><span data-stu-id="7905b-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="7905b-256">`[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="7905b-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="7905b-257">`[JavaContainer <String>]`: Java 컨테이너.</span><span class="sxs-lookup"><span data-stu-id="7905b-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="7905b-258">`[JavaContainerVersion <String>]`: Java 컨테이너 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="7905b-259">`[JavaVersion <String>]`: Java 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="7905b-260">`[LimitMaxDiskSizeInMb <Int64?>]`: 최대 허용 디스크 크기 사용량 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="7905b-261">`[LimitMaxMemoryInMb <Int64?>]`: 허용 되는 최대 메모리 사용량 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="7905b-262">`[LimitMaxPercentageCpu <Double?>]`: 허용 되는 최대 CPU 사용 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="7905b-263">`[LinuxFxVersion <String>]`: Linux 앱 프레임 워크 및 버전</span><span class="sxs-lookup"><span data-stu-id="7905b-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="7905b-264">`[LoadBalancing <SiteLoadBalancing?>]`: 사이트 로드 밸런싱.</span><span class="sxs-lookup"><span data-stu-id="7905b-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="7905b-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용 하도록 설정 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="7905b-267">`[MachineKeyDecryption <String>]`: 암호 해독에 사용 되는 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="7905b-268">`[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="7905b-269">`[MachineKeyValidation <String>]`: MachineKey 유효성 검사.</span><span class="sxs-lookup"><span data-stu-id="7905b-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="7905b-270">`[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="7905b-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리 되는 파이프라인 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="7905b-272">`[ManagedServiceIdentityId <Int32?>]`: 관리 되는 서비스 Id Id</span><span class="sxs-lookup"><span data-stu-id="7905b-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="7905b-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 TLS의 최소 버전을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="7905b-274">`[NetFrameworkVersion <String>]`: .NET Framework 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="7905b-275">`[NodeVersion <String>]`: Node.js 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="7905b-276">`[NumberOfWorker <Int32?>]`: 작업자 수.</span><span class="sxs-lookup"><span data-stu-id="7905b-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="7905b-277">`[PhpVersion <String>]`: PHP 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="7905b-278">`[PowerShellVersion <String>]`: PowerShell의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="7905b-279">`[PreWarmedInstanceCount <Int32?>]`: PreWarmed 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="7905b-280">이 설정은 사용량과 탄력적 요금제에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="7905b-281">`[PublishingUsername <String>]`: 게시 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="7905b-282">`[PushKind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="7905b-283">`[PythonVersion <String>]`: Python의 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="7905b-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-285">`[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전.</span><span class="sxs-lookup"><span data-stu-id="7905b-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="7905b-286">`[RequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="7905b-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="7905b-287">`[RequestTimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="7905b-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="7905b-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용 하도록 설정 하면 이 고, 그렇지 않으면 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-289">`[RequestTracingExpirationTime <DateTime?>]`: 추적 만료 시간을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="7905b-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Scm에 대 한 IP 보안 제한.</span><span class="sxs-lookup"><span data-stu-id="7905b-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="7905b-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Scm이 main을 사용할 수 있는 IP 보안 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="7905b-292">`[ScmType <ScmType?>]`: SCM 유형.</span><span class="sxs-lookup"><span data-stu-id="7905b-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="7905b-293">`[SlowRequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="7905b-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="7905b-294">`[SlowRequestTimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="7905b-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="7905b-295">`[SlowRequestTimeTaken <String>]`: 소요 시간.</span><span class="sxs-lookup"><span data-stu-id="7905b-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="7905b-296">`[TagWhitelistJson <String>]`: 푸시 등록 끝점에서 사용 하는 허용 목록 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="7905b-297">`[TagsRequiringAuth <String>]`: 푸시 등록 끝점에서 사용자 인증을 사용 해야 하는 태그 목록이 포함 된 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="7905b-298">태그는 영숫자 문자로 구성 되며 ' _ ', ' @ ', ' # ', '. ', ': ', '-'로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="7905b-299">PushRequestHandler에서 유효성 검사를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="7905b-300">`[TracingOption <String>]`: 추적 옵션</span><span class="sxs-lookup"><span data-stu-id="7905b-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="7905b-301">`[TriggerPrivateBytesInKb <Int32?>]`: 전용 바이트를 기준으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="7905b-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기준으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="7905b-303">`[Count <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="7905b-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="7905b-304">`[Status <Int32?>]`: HTTP 상태 코드.</span><span class="sxs-lookup"><span data-stu-id="7905b-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="7905b-305">`[SubStatus <Int32?>]`: 하위 상태 요청</span><span class="sxs-lookup"><span data-stu-id="7905b-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="7905b-306">`[TimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="7905b-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="7905b-307">`[Win32Status <Int32?>]`: Win32 오류 코드.</span><span class="sxs-lookup"><span data-stu-id="7905b-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="7905b-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 비트 작업자 프로세스를 사용 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-309">`[VirtualApplication <IVirtualApplication[]>]`: 가상 응용 프로그램.</span><span class="sxs-lookup"><span data-stu-id="7905b-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="7905b-310">`[PhysicalPath <String>]`: 실제 경로.</span><span class="sxs-lookup"><span data-stu-id="7905b-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="7905b-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="7905b-312">`[VirtualDirectory <IVirtualDirectory[]>]`: 가상 응용 프로그램의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="7905b-313">`[PhysicalPath <String>]`: 실제 경로.</span><span class="sxs-lookup"><span data-stu-id="7905b-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="7905b-314">`[VirtualPath <String>]`: 가상 응용 프로그램 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="7905b-315">`[VirtualPath <String>]`: 가상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="7905b-316">`[VnetName <String>]`: 가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="7905b-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="7905b-318">`[WindowsFxVersion <String>]`: 크 세 앱 프레임 워크 및 버전</span><span class="sxs-lookup"><span data-stu-id="7905b-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="7905b-319">`[XManagedServiceIdentityId <Int32?>]`: 관리 되는 명시적 서비스 Id Id</span><span class="sxs-lookup"><span data-stu-id="7905b-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="7905b-320">`[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="7905b-321">`[DailyMemoryTimeQuota <Int32?>]`: 허용 되는 최대 메모리 시간 할당량 (동적 앱에만 해당).</span><span class="sxs-lookup"><span data-stu-id="7905b-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="7905b-322">`[Enabled <Boolean?>]`: <code>true</code> 앱을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="7905b-323">이 값을 false로 설정 하면 앱을 사용할 수 없게 됩니다 (앱을 오프 라인 상태로 전환).</span><span class="sxs-lookup"><span data-stu-id="7905b-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="7905b-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL 상태는 앱의 호스트 이름에 대 한 SSL 바인딩을 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="7905b-325">`[HostType <HostType?>]`: 호스트 이름이 표준 또는 리포지토리 호스트 이름 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="7905b-326">`[Name <String>]`이름의.</span><span class="sxs-lookup"><span data-stu-id="7905b-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="7905b-327">`[SslState <SslState?>]`: SSL 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="7905b-328">`[Thumbprint <String>]`: SSL 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="7905b-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="7905b-329">`[ToUpdate <Boolean?>]`: <code>true</code> 기존 호스트 이름을 업데이트 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="7905b-330">`[VirtualIP <String>]`: IP 기반 SSL을 사용 하는 경우 호스트 이름에 가상 IP 주소를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="7905b-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> 앱의 공용 호스트 이름을 사용 하지 않도록 설정 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="7905b-332"><code>true</code>앱이 API management 프로세스를 통해서만 액세스할 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="7905b-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="7905b-333">`[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="7905b-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: 웹 사이트가 https 요청만 수락 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="7905b-335">Http 요청에 대 한 문제 리디렉션</span><span class="sxs-lookup"><span data-stu-id="7905b-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="7905b-336">`[HyperV <Boolean?>]`: Hyper-v 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="7905b-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="7905b-337">`[IdentityType <ManagedServiceIdentityType?>]`: 관리 되는 서비스 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="7905b-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결 된 사용자 할당 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="7905b-339">사용자 id 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="7905b-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7905b-341">`[IsXenon <Boolean?>]`: 구식: Hyper-v 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="7905b-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="7905b-342">`[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드</span><span class="sxs-lookup"><span data-stu-id="7905b-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="7905b-343">`[Reserved <Boolean?>]`: <code>true</code> 예약 된 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> 앱이 중지 되 면 SCM (KUDU) 사이트를 중지 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7905b-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="7905b-345">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="7905b-346">`[ServerFarmId <String>]`: 연결 된 앱 서비스 계획의 리소스 ID: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" 형식으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7905b-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="7905b-347">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7905b-347">RELATED LINKS</span></span>
