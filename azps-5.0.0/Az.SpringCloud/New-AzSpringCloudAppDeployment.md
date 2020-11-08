---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215233"
---
# <span data-ttu-id="d0f1f-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d0f1f-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d0f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f1f-103">새 배포를 만들거나 종료 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="d0f1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0f1f-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d0f1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f1f-106">새 배포를 만들거나 종료 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="d0f1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d0f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="d0f1f-108">예제 1: 예제 1: 스프링 클라우드 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="d0f1f-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="d0f1f-109">스프링 클라우드 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="d0f1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="d0f1f-110">PARAMETERS</span></span>

### <span data-ttu-id="d0f1f-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="d0f1f-111">-AppName</span></span>
<span data-ttu-id="d0f1f-112">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="d0f1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0f1f-113">-AsJob</span></span>
<span data-ttu-id="d0f1f-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0f1f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d0f1f-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="d0f1f-115">-Cpu</span></span>
<span data-ttu-id="d0f1f-116">필수 CPU</span><span class="sxs-lookup"><span data-stu-id="d0f1f-116">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f1f-117">-DefaultProfile</span></span>
<span data-ttu-id="d0f1f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f1f-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="d0f1f-119">-EnvironmentVariable</span></span>
<span data-ttu-id="d0f1f-120">환경 변수 컬렉션</span><span class="sxs-lookup"><span data-stu-id="d0f1f-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="d0f1f-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="d0f1f-121">-JvmOption</span></span>
<span data-ttu-id="d0f1f-122">JVM 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0f1f-122">JVM parameter</span></span>

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

### <span data-ttu-id="d0f1f-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="d0f1f-123">-MemoryInGb</span></span>
<span data-ttu-id="d0f1f-124">필요한 메모리 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="d0f1f-124">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d0f1f-125">-Name</span></span>
<span data-ttu-id="d0f1f-126">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0f1f-127">-NoWait</span></span>
<span data-ttu-id="d0f1f-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0f1f-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0f1f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f1f-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0f1f-130">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d0f1f-131">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d0f1f-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="d0f1f-132">-RuntimeVersion</span></span>
<span data-ttu-id="d0f1f-133">런타임 버전</span><span class="sxs-lookup"><span data-stu-id="d0f1f-133">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d0f1f-134">-ServiceName</span></span>
<span data-ttu-id="d0f1f-135">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d0f1f-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="d0f1f-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="d0f1f-137">다중 모듈 프로젝트의 배포에 사용 되는 아티팩트의 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="d0f1f-138">이는 대상 모듈/프로젝트에 대 한 상대 경로를 지켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="d0f1f-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="d0f1f-139">-SourceRelativePath</span></span>
<span data-ttu-id="d0f1f-140">원본을 저장 하는 저장소의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="d0f1f-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d0f1f-141">-SourceType</span></span>
<span data-ttu-id="d0f1f-142">업로드 된 원본 유형</span><span class="sxs-lookup"><span data-stu-id="d0f1f-142">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="d0f1f-143">-SourceVersion</span></span>
<span data-ttu-id="d0f1f-144">원본 버전</span><span class="sxs-lookup"><span data-stu-id="d0f1f-144">Version of the source</span></span>

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

### <span data-ttu-id="d0f1f-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0f1f-145">-SubscriptionId</span></span>
<span data-ttu-id="d0f1f-146">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0f1f-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1f-148">-확인</span><span class="sxs-lookup"><span data-stu-id="d0f1f-148">-Confirm</span></span>
<span data-ttu-id="d0f1f-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f1f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f1f-150">-WhatIf</span></span>
<span data-ttu-id="d0f1f-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f1f-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f1f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f1f-153">CommonParameters</span></span>
<span data-ttu-id="d0f1f-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f1f-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f1f-156">입력</span><span class="sxs-lookup"><span data-stu-id="d0f1f-156">INPUTS</span></span>

## <span data-ttu-id="d0f1f-157">출력</span><span class="sxs-lookup"><span data-stu-id="d0f1f-157">OUTPUTS</span></span>

### <span data-ttu-id="d0f1f-158">SpringCloud. PowerShell. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="d0f1f-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="d0f1f-159">상속자</span><span class="sxs-lookup"><span data-stu-id="d0f1f-159">NOTES</span></span>

<span data-ttu-id="d0f1f-160">별칭과</span><span class="sxs-lookup"><span data-stu-id="d0f1f-160">ALIASES</span></span>

## <span data-ttu-id="d0f1f-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0f1f-161">RELATED LINKS</span></span>
