---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: cb5de7f8e0e484c5b9080e3a50871cddca5af173
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531495"
---
# <span data-ttu-id="dfe12-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="dfe12-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="dfe12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe12-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe12-103">Application insights 가져오기 지속적인 application insights 리소스에 대 한 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="dfe12-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfe12-104">SYNTAX</span></span>

### <span data-ttu-id="dfe12-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dfe12-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfe12-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe12-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfe12-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe12-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe12-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dfe12-108">DESCRIPTION</span></span>
<span data-ttu-id="dfe12-109">Application insights 가져오기 지속적인 application insights 리소스에 대 한 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="dfe12-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="dfe12-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dfe12-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe12-111">예제 1 application insights 리소스에 대 한 연속 내보내기 가져오기</span><span class="sxs-lookup"><span data-stu-id="dfe12-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="dfe12-112">리소스 그룹 "testgroup"에서 "test" 라는 리소스에 대 한 application insights 연속 내보내기 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="dfe12-113">예제 2 application insights 리소스의 연속 내보내기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="dfe12-114">리소스 그룹 "testgroup"에서 "test" 리소스에 대 한 내보내기 id가 "ZJrfffySPdtG3ESn3iRxVIEFuNY =" 인 application insights 연속 내보내기 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="dfe12-115">변수</span><span class="sxs-lookup"><span data-stu-id="dfe12-115">PARAMETERS</span></span>

### <span data-ttu-id="dfe12-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dfe12-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="dfe12-117">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="dfe12-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe12-118">-DefaultProfile</span></span>
<span data-ttu-id="dfe12-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="dfe12-120">-ExportId</span></span>
<span data-ttu-id="dfe12-121">Application Insights 연속 내보내기 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-122">-이름</span><span class="sxs-lookup"><span data-stu-id="dfe12-122">-Name</span></span>
<span data-ttu-id="dfe12-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe12-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfe12-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe12-126">-ResourceId</span></span>
<span data-ttu-id="dfe12-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe12-128">CommonParameters</span></span>
<span data-ttu-id="dfe12-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe12-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe12-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe12-131">입력</span><span class="sxs-lookup"><span data-stu-id="dfe12-131">INPUTS</span></span>

### <span data-ttu-id="dfe12-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="dfe12-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="dfe12-133">매개 변수: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dfe12-133">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="dfe12-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfe12-134">System.String</span></span>

## <span data-ttu-id="dfe12-135">출력</span><span class="sxs-lookup"><span data-stu-id="dfe12-135">OUTPUTS</span></span>

### <span data-ttu-id="dfe12-136">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="dfe12-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="dfe12-137">상속자</span><span class="sxs-lookup"><span data-stu-id="dfe12-137">NOTES</span></span>

## <span data-ttu-id="dfe12-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfe12-138">RELATED LINKS</span></span>