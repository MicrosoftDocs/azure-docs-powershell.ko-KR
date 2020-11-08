---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: e304b9394878c734f51988816ef512158957feab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213944"
---
# <span data-ttu-id="d6689-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="d6689-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="d6689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6689-102">SYNOPSIS</span></span>
<span data-ttu-id="d6689-103">서비스 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="d6689-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6689-104">SYNTAX</span></span>

### <span data-ttu-id="d6689-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6689-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6689-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d6689-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6689-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6689-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6689-108">List1</span><span class="sxs-lookup"><span data-stu-id="d6689-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6689-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d6689-109">DESCRIPTION</span></span>
<span data-ttu-id="d6689-110">서비스 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="d6689-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d6689-111">EXAMPLES</span></span>

### <span data-ttu-id="d6689-112">예제 1: 이름으로 스프링 클라우드 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d6689-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="d6689-113">이름으로 스프링 클라우드 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d6689-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="d6689-114">예제 2: 모든 스프링 클라우드 서비스를 리소스 그룹 아래에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="d6689-115">모든 스프링 클라우드 서비스를 리소스 그룹 아래에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="d6689-116">변수</span><span class="sxs-lookup"><span data-stu-id="d6689-116">PARAMETERS</span></span>

### <span data-ttu-id="d6689-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6689-117">-DefaultProfile</span></span>
<span data-ttu-id="d6689-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6689-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6689-119">-InputObject</span></span>
<span data-ttu-id="d6689-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6689-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d6689-121">-Name</span></span>
<span data-ttu-id="d6689-122">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6689-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6689-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6689-124">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d6689-125">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6689-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6689-126">-SubscriptionId</span></span>
<span data-ttu-id="d6689-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6689-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6689-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6689-129">CommonParameters</span></span>
<span data-ttu-id="d6689-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6689-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6689-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6689-132">입력</span><span class="sxs-lookup"><span data-stu-id="d6689-132">INPUTS</span></span>

### <span data-ttu-id="d6689-133">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6689-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d6689-134">출력</span><span class="sxs-lookup"><span data-stu-id="d6689-134">OUTPUTS</span></span>

### <span data-ttu-id="d6689-135">SpringCloud. PowerShell. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="d6689-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="d6689-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d6689-136">NOTES</span></span>

<span data-ttu-id="d6689-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="d6689-137">ALIASES</span></span>

<span data-ttu-id="d6689-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d6689-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6689-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6689-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6689-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6689-141">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6689-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6689-142">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d6689-143">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d6689-144">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d6689-145">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d6689-146">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d6689-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d6689-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6689-148">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="d6689-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d6689-149">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d6689-150">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d6689-151">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d6689-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d6689-153">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6689-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6689-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6689-154">RELATED LINKS</span></span>
