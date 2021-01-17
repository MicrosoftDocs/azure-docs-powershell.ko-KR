---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330746"
---
# <span data-ttu-id="40602-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="40602-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="40602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40602-102">SYNOPSIS</span></span>
<span data-ttu-id="40602-103">연결 삭제</span><span class="sxs-lookup"><span data-stu-id="40602-103">Delete an association.</span></span>

## <span data-ttu-id="40602-104">구문</span><span class="sxs-lookup"><span data-stu-id="40602-104">SYNTAX</span></span>

### <span data-ttu-id="40602-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="40602-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40602-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40602-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40602-107">설명</span><span class="sxs-lookup"><span data-stu-id="40602-107">DESCRIPTION</span></span>
<span data-ttu-id="40602-108">연결 삭제</span><span class="sxs-lookup"><span data-stu-id="40602-108">Delete an association.</span></span>

## <span data-ttu-id="40602-109">예제</span><span class="sxs-lookup"><span data-stu-id="40602-109">EXAMPLES</span></span>

### <span data-ttu-id="40602-110">예제 1: 사용자 지정 공급자 연결 제거</span><span class="sxs-lookup"><span data-stu-id="40602-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="40602-111">사용자 지정 공급자 연결 제거</span><span class="sxs-lookup"><span data-stu-id="40602-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="40602-112">예제 2: Piping과 사용자 지정 공급자 연결 제거</span><span class="sxs-lookup"><span data-stu-id="40602-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="40602-113">파이핑 및 PassThru 기능을 사용하여 성공 또는 실패를 나타내는 사용자 지정 공급자 연결 제거</span><span class="sxs-lookup"><span data-stu-id="40602-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="40602-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40602-114">PARAMETERS</span></span>

### <span data-ttu-id="40602-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40602-115">-AsJob</span></span>
<span data-ttu-id="40602-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="40602-116">Run the command as a job</span></span>

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

### <span data-ttu-id="40602-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40602-117">-DefaultProfile</span></span>
<span data-ttu-id="40602-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40602-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40602-119">-InputObject</span></span>
<span data-ttu-id="40602-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="40602-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40602-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40602-121">-Name</span></span>
<span data-ttu-id="40602-122">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40602-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40602-123">-NoWait</span></span>
<span data-ttu-id="40602-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="40602-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40602-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40602-125">-PassThru</span></span>
<span data-ttu-id="40602-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="40602-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="40602-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="40602-127">-Scope</span></span>
<span data-ttu-id="40602-128">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-128">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40602-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40602-129">-Confirm</span></span>
<span data-ttu-id="40602-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40602-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40602-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40602-131">-WhatIf</span></span>
<span data-ttu-id="40602-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="40602-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40602-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40602-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40602-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40602-134">CommonParameters</span></span>
<span data-ttu-id="40602-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40602-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40602-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40602-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40602-137">입력</span><span class="sxs-lookup"><span data-stu-id="40602-137">INPUTS</span></span>

### <span data-ttu-id="40602-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="40602-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="40602-139">출력</span><span class="sxs-lookup"><span data-stu-id="40602-139">OUTPUTS</span></span>

### <span data-ttu-id="40602-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40602-140">System.Boolean</span></span>

## <span data-ttu-id="40602-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40602-141">NOTES</span></span>

<span data-ttu-id="40602-142">별칭</span><span class="sxs-lookup"><span data-stu-id="40602-142">ALIASES</span></span>

<span data-ttu-id="40602-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="40602-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40602-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="40602-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40602-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40602-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40602-146">INPUTOBJECT: <ICustomProvidersIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="40602-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40602-147">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="40602-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="40602-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40602-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="40602-150">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="40602-151">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="40602-152">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40602-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="40602-153">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="40602-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="40602-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40602-154">RELATED LINKS</span></span>
