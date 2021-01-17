---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332594"
---
# <span data-ttu-id="aaba2-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="aaba2-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="aaba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaba2-102">SYNOPSIS</span></span>
<span data-ttu-id="aaba2-103">배포를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="aaba2-104">구문</span><span class="sxs-lookup"><span data-stu-id="aaba2-104">SYNTAX</span></span>

### <span data-ttu-id="aaba2-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="aaba2-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aaba2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaba2-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaba2-107">설명</span><span class="sxs-lookup"><span data-stu-id="aaba2-107">DESCRIPTION</span></span>
<span data-ttu-id="aaba2-108">배포를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="aaba2-109">예제</span><span class="sxs-lookup"><span data-stu-id="aaba2-109">EXAMPLES</span></span>

### <span data-ttu-id="aaba2-110">예제 1: 이름으로 Spring Cloud 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="aaba2-111">이름으로 Spring Cloud 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="aaba2-112">예제 2: 파이프에서 Spring Cloud 배포 제거</span><span class="sxs-lookup"><span data-stu-id="aaba2-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="aaba2-113">파이프에서 Spring Cloud 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="aaba2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaba2-114">PARAMETERS</span></span>

### <span data-ttu-id="aaba2-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="aaba2-115">-AppName</span></span>
<span data-ttu-id="aaba2-116">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="aaba2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaba2-117">-AsJob</span></span>
<span data-ttu-id="aaba2-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="aaba2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="aaba2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaba2-119">-DefaultProfile</span></span>
<span data-ttu-id="aaba2-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaba2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaba2-121">-InputObject</span></span>
<span data-ttu-id="aaba2-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="aaba2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaba2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aaba2-123">-Name</span></span>
<span data-ttu-id="aaba2-124">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaba2-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aaba2-125">-NoWait</span></span>
<span data-ttu-id="aaba2-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="aaba2-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aaba2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaba2-127">-PassThru</span></span>
<span data-ttu-id="aaba2-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aaba2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaba2-129">-ResourceGroupName</span></span>
<span data-ttu-id="aaba2-130">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aaba2-131">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aaba2-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aaba2-132">-ServiceName</span></span>
<span data-ttu-id="aaba2-133">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="aaba2-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaba2-134">-SubscriptionId</span></span>
<span data-ttu-id="aaba2-135">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aaba2-136">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaba2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaba2-137">-Confirm</span></span>
<span data-ttu-id="aaba2-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaba2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaba2-139">-WhatIf</span></span>
<span data-ttu-id="aaba2-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aaba2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaba2-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaba2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaba2-142">CommonParameters</span></span>
<span data-ttu-id="aaba2-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaba2-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aaba2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaba2-145">입력</span><span class="sxs-lookup"><span data-stu-id="aaba2-145">INPUTS</span></span>

### <span data-ttu-id="aaba2-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="aaba2-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="aaba2-147">출력</span><span class="sxs-lookup"><span data-stu-id="aaba2-147">OUTPUTS</span></span>

### <span data-ttu-id="aaba2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aaba2-148">System.Boolean</span></span>

## <span data-ttu-id="aaba2-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaba2-149">NOTES</span></span>

<span data-ttu-id="aaba2-150">별칭</span><span class="sxs-lookup"><span data-stu-id="aaba2-150">ALIASES</span></span>

<span data-ttu-id="aaba2-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="aaba2-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaba2-152">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaba2-153">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaba2-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaba2-154">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="aaba2-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaba2-155">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="aaba2-156">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="aaba2-157">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="aaba2-158">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="aaba2-159">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="aaba2-160">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="aaba2-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaba2-161">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="aaba2-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="aaba2-162">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aaba2-163">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aaba2-164">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="aaba2-165">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="aaba2-166">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="aaba2-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aaba2-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaba2-167">RELATED LINKS</span></span>
