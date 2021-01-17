---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 559cff58ac8d6c3f3d8f116b6147d6f4c2a4378d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330945"
---
# <span data-ttu-id="eb0fe-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="eb0fe-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="eb0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0fe-103">msixpackage를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-103">Get a msixpackage.</span></span>

## <span data-ttu-id="eb0fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb0fe-104">SYNTAX</span></span>

### <span data-ttu-id="eb0fe-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="eb0fe-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb0fe-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="eb0fe-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb0fe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb0fe-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb0fe-108">설명</span><span class="sxs-lookup"><span data-stu-id="eb0fe-108">DESCRIPTION</span></span>
<span data-ttu-id="eb0fe-109">msixpackage를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-109">Get a msixpackage.</span></span>

## <span data-ttu-id="eb0fe-110">예제</span><span class="sxs-lookup"><span data-stu-id="eb0fe-110">EXAMPLES</span></span>

### <span data-ttu-id="eb0fe-111">예제 1: 이름에 의해 MSIX 패키지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="eb0fe-112">이 명령은 HostPool에서 MSIX 패키지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="eb0fe-113">예제 2: MSIX 패키지 나열</span><span class="sxs-lookup"><span data-stu-id="eb0fe-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="eb0fe-114">이 명령은 HostPool의 MSIX 패키지를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="eb0fe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb0fe-115">PARAMETERS</span></span>

### <span data-ttu-id="eb0fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0fe-116">-DefaultProfile</span></span>
<span data-ttu-id="eb0fe-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb0fe-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="eb0fe-118">-FullName</span></span>
<span data-ttu-id="eb0fe-119">지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0fe-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="eb0fe-120">-HostPoolName</span></span>
<span data-ttu-id="eb0fe-121">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-121">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb0fe-122">-InputObject</span></span>
<span data-ttu-id="eb0fe-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb0fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb0fe-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-125">The name of the resource group.</span></span>
<span data-ttu-id="eb0fe-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0fe-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb0fe-127">-SubscriptionId</span></span>
<span data-ttu-id="eb0fe-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0fe-129">CommonParameters</span></span>
<span data-ttu-id="eb0fe-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0fe-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0fe-132">입력</span><span class="sxs-lookup"><span data-stu-id="eb0fe-132">INPUTS</span></span>

### <span data-ttu-id="eb0fe-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="eb0fe-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="eb0fe-134">출력</span><span class="sxs-lookup"><span data-stu-id="eb0fe-134">OUTPUTS</span></span>

### <span data-ttu-id="eb0fe-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="eb0fe-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="eb0fe-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb0fe-136">NOTES</span></span>

<span data-ttu-id="eb0fe-137">별칭</span><span class="sxs-lookup"><span data-stu-id="eb0fe-137">ALIASES</span></span>

<span data-ttu-id="eb0fe-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="eb0fe-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb0fe-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb0fe-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb0fe-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="eb0fe-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb0fe-142">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="eb0fe-143">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="eb0fe-144">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="eb0fe-145">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="eb0fe-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="eb0fe-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb0fe-147">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="eb0fe-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eb0fe-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="eb0fe-150">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="eb0fe-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb0fe-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eb0fe-152">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="eb0fe-153">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="eb0fe-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="eb0fe-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb0fe-154">RELATED LINKS</span></span>
