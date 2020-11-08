---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213378"
---
# <span data-ttu-id="be59c-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="be59c-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="be59c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be59c-102">SYNOPSIS</span></span>
<span data-ttu-id="be59c-103">서비스 인스턴스의 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="be59c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be59c-104">SYNTAX</span></span>

### <span data-ttu-id="be59c-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="be59c-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be59c-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be59c-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be59c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be59c-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be59c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="be59c-108">DESCRIPTION</span></span>
<span data-ttu-id="be59c-109">지정 된 구독 또는 리소스 그룹 내에서 만든 기존 healthcareApis fa r 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="be59c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="be59c-110">EXAMPLES</span></span>

### <span data-ttu-id="be59c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="be59c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="be59c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="be59c-112">Example 2</span></span>

<span data-ttu-id="be59c-113">제공 된 리소스 그룹의 모든 HealthcareApis 서비스에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="be59c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="be59c-114">Example 3</span></span>

<span data-ttu-id="be59c-115">지정 된 구독에서 모든 HealthcareApis 서비스에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="be59c-116">변수</span><span class="sxs-lookup"><span data-stu-id="be59c-116">PARAMETERS</span></span>

### <span data-ttu-id="be59c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be59c-117">-DefaultProfile</span></span>
<span data-ttu-id="be59c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be59c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="be59c-119">-Name</span></span>
<span data-ttu-id="be59c-120">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be59c-121">-ResourceGroupName</span></span>
<span data-ttu-id="be59c-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be59c-123">-ResourceId</span></span>
<span data-ttu-id="be59c-124">리소스 Id 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-124">Resource Id Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be59c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be59c-125">CommonParameters</span></span>
<span data-ttu-id="be59c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be59c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be59c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be59c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be59c-128">입력</span><span class="sxs-lookup"><span data-stu-id="be59c-128">INPUTS</span></span>

### <span data-ttu-id="be59c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be59c-129">System.String</span></span>

## <span data-ttu-id="be59c-130">출력</span><span class="sxs-lookup"><span data-stu-id="be59c-130">OUTPUTS</span></span>

### <span data-ttu-id="be59c-131">HealthcareApisService. PSHealthcareApisService/.</span><span class="sxs-lookup"><span data-stu-id="be59c-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="be59c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="be59c-132">NOTES</span></span>

## <span data-ttu-id="be59c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be59c-133">RELATED LINKS</span></span>