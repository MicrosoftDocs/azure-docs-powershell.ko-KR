---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049252"
---
# <span data-ttu-id="ec972-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-101">New-AzApiManagement</span></span>

## <span data-ttu-id="ec972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec972-102">SYNOPSIS</span></span>
<span data-ttu-id="ec972-103">API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="ec972-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec972-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec972-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec972-105">DESCRIPTION</span></span>
<span data-ttu-id="ec972-106">**AzApiManagement** Cmdlet은 Azure api MANAGEMENT에서 API management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="ec972-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec972-107">EXAMPLES</span></span>

### <span data-ttu-id="ec972-108">예제 1: 개발자 계층 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ec972-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="ec972-109">이 명령은 개발자 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="ec972-110">명령은 조직과 관리자 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="ec972-111">명령에서 *SKU* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="ec972-112">따라서 cmdlet은 기본 개발자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="ec972-113">예제 2: 세 개의 단위가 있는 표준 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ec972-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="ec972-114">이 명령은 세 개의 단위가 있는 표준 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="ec972-115">예제 3: 소비 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ec972-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="ec972-116">이 명령은 서유럽에서 클라이언트 인증서를 사용 하 여 소비 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="ec972-117">예제 4: 외부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ec972-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="ec972-118">이 명령은 미국 내에서 마스터 영역이 있는 외부 연결 게이트웨이 끝점을 사용 하 여 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="ec972-119">예제 5: 내부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ec972-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="ec972-120">이 명령은 미국 내에서 마스터 영역이 있는 내부 연결 게이트웨이 끝점을 사용 하는 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="ec972-121">예제 6: API Management 서비스를 만들고 TLS 1.0 프로토콜을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="ec972-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="ec972-122">이 명령은 표준 SKU Api 관리 서비스를 만들고 프런트 엔드 클라이언트에서 ApiManagement Gateway와 백 엔드 간에 ApiManagement Gateway 및 백 엔드 클라이언트로 TLS 1.0을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="ec972-123">변수</span><span class="sxs-lookup"><span data-stu-id="ec972-123">PARAMETERS</span></span>

### <span data-ttu-id="ec972-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="ec972-124">-AdditionalRegions</span></span>
<span data-ttu-id="ec972-125">Azure API Management의 추가 배포 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-125">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="ec972-126">-AdminEmail</span></span>
<span data-ttu-id="ec972-127">API Management 시스템에서 보내는 모든 알림에 대 한 원래 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-128">용량</span><span class="sxs-lookup"><span data-stu-id="ec972-128">-Capacity</span></span>
<span data-ttu-id="ec972-129">Azure API Management 서비스의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="ec972-130">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-130">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec972-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="ec972-132">사용자 지정 호스트 이름 구성</span><span class="sxs-lookup"><span data-stu-id="ec972-132">Custom hostname configurations.</span></span> <span data-ttu-id="ec972-133">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-133">Default value is $null.</span></span> <span data-ttu-id="ec972-134">$Null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-134">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec972-135">-DefaultProfile</span></span>
<span data-ttu-id="ec972-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec972-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ec972-137">-EnableClientCertificate</span></span>
<span data-ttu-id="ec972-138">SKU ApiManagement 서비스 사용량에만 사용 되는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="ec972-139">이렇게 하면 게이트웨이에 대 한 각 요청에 클라이언트 인증서가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="ec972-140">이렇게 하면 게이트웨이의 정책에서 인증서를 인증 하는 기능도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="ec972-141">-위치</span><span class="sxs-lookup"><span data-stu-id="ec972-141">-Location</span></span>
<span data-ttu-id="ec972-142">Api Management 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="ec972-143">유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="ec972-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-144">-이름</span><span class="sxs-lookup"><span data-stu-id="ec972-144">-Name</span></span>
<span data-ttu-id="ec972-145">API Management 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-145">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-146">-조직</span><span class="sxs-lookup"><span data-stu-id="ec972-146">-Organization</span></span>
<span data-ttu-id="ec972-147">조직의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="ec972-148">API Management는 전자 메일 알림에서 개발자 포털에서이 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-148">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec972-149">-ResourceGroupName</span></span>
<span data-ttu-id="ec972-150">이 cmdlet이 API Management 배포를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="ec972-151">-Sku</span></span>
<span data-ttu-id="ec972-152">API Management 서비스의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="ec972-153">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-153">Valid values are:</span></span> 
- <span data-ttu-id="ec972-154">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="ec972-154">Developer</span></span> 
- <span data-ttu-id="ec972-155">표준이</span><span class="sxs-lookup"><span data-stu-id="ec972-155">Standard</span></span> 
- <span data-ttu-id="ec972-156">Premium 기본값은 개발자입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="ec972-157">-SslSetting</span></span>
<span data-ttu-id="ec972-158">ApiManagement 서비스의 Ssl 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="ec972-159">기본값은 $null 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ec972-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ec972-161">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec972-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec972-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="ec972-163">서비스에 설치 되도록 내부 CA에서 발급 한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="ec972-164">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-165">태그</span><span class="sxs-lookup"><span data-stu-id="ec972-165">-Tag</span></span>
<span data-ttu-id="ec972-166">태그 사전.</span><span class="sxs-lookup"><span data-stu-id="ec972-166">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ec972-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="ec972-168">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 사용자 Id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec972-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ec972-169">-VirtualNetwork</span></span>
<span data-ttu-id="ec972-170">마스터 Azure API Management 배포 영역의 가상 네트워크 구성</span><span class="sxs-lookup"><span data-stu-id="ec972-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="ec972-171">-VpnType</span></span>
<span data-ttu-id="ec972-172">ApiManagement 배포의 가상 네트워크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="ec972-173">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="ec972-173">Valid Values are</span></span> 
- <span data-ttu-id="ec972-174">"없음" (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec972-174">"None" (Default Value.</span></span> <span data-ttu-id="ec972-175">ApiManagement는 가상 네트워크의 일부가 아닙니다. ")</span><span class="sxs-lookup"><span data-stu-id="ec972-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="ec972-176">"외부" (인터넷이 연결 된 끝점을 보유 한 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="ec972-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="ec972-177">"내부" (인트라넷이 연결 된 끝점을 보유 하 고 있는 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="ec972-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec972-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec972-178">CommonParameters</span></span>
<span data-ttu-id="ec972-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec972-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec972-180">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec972-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec972-181">입력</span><span class="sxs-lookup"><span data-stu-id="ec972-181">INPUTS</span></span>

### <span data-ttu-id="ec972-182">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec972-182">System.String</span></span>

### <span data-ttu-id="ec972-183">시스템 Null 허용 ' 1 [[ApiManagement. PsApiManagementSku, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ec972-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec972-184">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="ec972-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec972-185">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="ec972-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="ec972-186">System.webserver. Dictionary ' 2 [[4.0.0.0], CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e], [System.webserver,, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec972-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec972-187">ApiManagement [] PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="ec972-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="ec972-188">ApiManagement [] PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ec972-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="ec972-189">ApiManagement [] PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="ec972-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="ec972-190">출력</span><span class="sxs-lookup"><span data-stu-id="ec972-190">OUTPUTS</span></span>

### <span data-ttu-id="ec972-191">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="ec972-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ec972-192">상속자</span><span class="sxs-lookup"><span data-stu-id="ec972-192">NOTES</span></span>

## <span data-ttu-id="ec972-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec972-193">RELATED LINKS</span></span>

[<span data-ttu-id="ec972-194">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="ec972-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="ec972-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="ec972-197">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="ec972-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec972-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

