---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 05bf93584fcc39f239877e2568cb88b243b1e820
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216145"
---
# <span data-ttu-id="9da66-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9da66-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9da66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9da66-102">SYNOPSIS</span></span>
<span data-ttu-id="9da66-103">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="9da66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9da66-104">SYNTAX</span></span>

### <span data-ttu-id="9da66-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="9da66-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da66-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9da66-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SigninTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9da66-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9da66-107">DESCRIPTION</span></span>
<span data-ttu-id="9da66-108">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="9da66-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9da66-109">EXAMPLES</span></span>

### <span data-ttu-id="9da66-110">예제 1: facebook Id 공급자 업데이트</span><span class="sxs-lookup"><span data-stu-id="9da66-110">Example 1: Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="9da66-111">Cmdlet은 Facebook Id 공급자의 클라이언트 비밀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

### <span data-ttu-id="9da66-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9da66-112">Example 2</span></span>

<span data-ttu-id="9da66-113">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-113">Updates the Configuration of an existing Identity Provider.</span></span> <span data-ttu-id="9da66-114">생성</span><span class="sxs-lookup"><span data-stu-id="9da66-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementIdentityProvider -AllowedTenants 'samirtestbc.onmicrosoft.com' -Authority <String> -ClientId 'clientid' -ClientSecret 'updatedSecret' -Context <PsApiManagementContext> -PasswordResetPolicyName <String> -ProfileEditingPolicyName <String> -SigninPolicyName <String> -SignupPolicyName B2C_1_signup-policy -Type Facebook
```

## <span data-ttu-id="9da66-115">변수</span><span class="sxs-lookup"><span data-stu-id="9da66-115">PARAMETERS</span></span>

### <span data-ttu-id="9da66-116">-AllowedTenants 넌 트</span><span class="sxs-lookup"><span data-stu-id="9da66-116">-AllowedTenants</span></span>
<span data-ttu-id="9da66-117">허용 되는 Azure Active Directory 테 넌 트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-117">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da66-118">-기관</span><span class="sxs-lookup"><span data-stu-id="9da66-118">-Authority</span></span>
<span data-ttu-id="9da66-119">AAD 또는 AAD B2C에 대 한 OpenID Connect 검색 끝점 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-119">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="9da66-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="9da66-121">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9da66-121">-ClientId</span></span>
<span data-ttu-id="9da66-122">외부 Id 공급자의 응용 프로그램에 대 한 클라이언트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-122">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="9da66-123">Facebook 로그인의 앱 ID, Google 로그인의 클라이언트 ID, Microsoft의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-123">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="9da66-124">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9da66-124">-ClientSecret</span></span>
<span data-ttu-id="9da66-125">로그인 요청을 인증 하는 데 사용 되는 외부 Id 공급자에 해당 하는 응용 프로그램의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-125">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="9da66-126">예를 들어 Facebook 로그인에 대 한 앱 비밀, Google 로그인의 API 키, Microsoft의 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-126">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="9da66-127">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9da66-127">-Context</span></span>
<span data-ttu-id="9da66-128">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-128">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9da66-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-129">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9da66-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da66-130">-DefaultProfile</span></span>
<span data-ttu-id="9da66-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9da66-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9da66-132">-InputObject</span></span>
<span data-ttu-id="9da66-133">PsApiManagementIdentityProvider의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-133">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="9da66-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-134">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9da66-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da66-135">-PassThru</span></span>
<span data-ttu-id="9da66-136">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementIdentityProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-136">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9da66-137">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="9da66-137">-PasswordResetPolicyName</span></span>
<span data-ttu-id="9da66-138">암호 재설정 정책 이름.</span><span class="sxs-lookup"><span data-stu-id="9da66-138">Password Reset Policy Name.</span></span> <span data-ttu-id="9da66-139">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-139">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9da66-140">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="9da66-141">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="9da66-141">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="9da66-142">프로필 편집 정책 이름</span><span class="sxs-lookup"><span data-stu-id="9da66-142">Profile Editing Policy Name.</span></span> <span data-ttu-id="9da66-143">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-143">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9da66-144">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="9da66-145">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="9da66-145">-SigninPolicyName</span></span>
<span data-ttu-id="9da66-146">로그인 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-146">Signin Policy Name.</span></span> <span data-ttu-id="9da66-147">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9da66-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="9da66-149">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="9da66-149">-SigninTenant</span></span>
<span data-ttu-id="9da66-150">테 넌 트가 아닌 AAD B2C에서 재정의 하도록 로그인 테 넌 트 `common`</span><span class="sxs-lookup"><span data-stu-id="9da66-150">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="9da66-151">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9da66-151">-SignupPolicyName</span></span>
<span data-ttu-id="9da66-152">등록 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-152">Signup Policy Name.</span></span> <span data-ttu-id="9da66-153">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-153">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9da66-154">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-154">This parameter is optional.</span></span>

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

### <span data-ttu-id="9da66-155">-Type</span><span class="sxs-lookup"><span data-stu-id="9da66-155">-Type</span></span>
<span data-ttu-id="9da66-156">기존 Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-156">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="9da66-157">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-157">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da66-158">-확인</span><span class="sxs-lookup"><span data-stu-id="9da66-158">-Confirm</span></span>
<span data-ttu-id="9da66-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da66-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da66-160">-WhatIf</span></span>
<span data-ttu-id="9da66-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9da66-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da66-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da66-163">CommonParameters</span></span>
<span data-ttu-id="9da66-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9da66-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da66-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9da66-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da66-166">입력</span><span class="sxs-lookup"><span data-stu-id="9da66-166">INPUTS</span></span>

### <span data-ttu-id="9da66-167">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9da66-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9da66-168">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="9da66-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="9da66-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9da66-169">System.String</span></span>

### <span data-ttu-id="9da66-170">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="9da66-170">System.String[]</span></span>

### <span data-ttu-id="9da66-171">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9da66-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9da66-172">출력</span><span class="sxs-lookup"><span data-stu-id="9da66-172">OUTPUTS</span></span>

### <span data-ttu-id="9da66-173">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9da66-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9da66-174">상속자</span><span class="sxs-lookup"><span data-stu-id="9da66-174">NOTES</span></span>

## <span data-ttu-id="9da66-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9da66-175">RELATED LINKS</span></span>

[<span data-ttu-id="9da66-176">새로운 AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9da66-176">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9da66-177">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9da66-177">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9da66-178">제거-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9da66-178">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)