---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: e6e1e2319ade47557ddf07f34a9371a4bbd532b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869298"
---
# <span data-ttu-id="98f02-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="98f02-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="98f02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f02-102">SYNOPSIS</span></span>
<span data-ttu-id="98f02-103">Application insights 가져오기 지속적인 application insights 리소스에 대 한 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="98f02-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="98f02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98f02-104">SYNTAX</span></span>

### <span data-ttu-id="98f02-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="98f02-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f02-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f02-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f02-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f02-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f02-108">설명은</span><span class="sxs-lookup"><span data-stu-id="98f02-108">DESCRIPTION</span></span>
<span data-ttu-id="98f02-109">Application insights 가져오기 지속적인 application insights 리소스에 대 한 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="98f02-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="98f02-110">예제의</span><span class="sxs-lookup"><span data-stu-id="98f02-110">EXAMPLES</span></span>

### <span data-ttu-id="98f02-111">예제 1 application insights 리소스에 대 한 연속 내보내기 가져오기</span><span class="sxs-lookup"><span data-stu-id="98f02-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="98f02-112">리소스 그룹 "testgroup"에서 "test" 라는 리소스에 대 한 application insights 연속 내보내기 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="98f02-113">예제 2 application insights 리소스의 연속 내보내기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="98f02-114">리소스 그룹 "testgroup"에서 "test" 리소스에 대 한 내보내기 id가 "ZJrfffySPdtG3ESn3iRxVIEFuNY =" 인 application insights 연속 내보내기 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="98f02-115">변수</span><span class="sxs-lookup"><span data-stu-id="98f02-115">PARAMETERS</span></span>

### <span data-ttu-id="98f02-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="98f02-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="98f02-117">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="98f02-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="98f02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f02-118">-DefaultProfile</span></span>
<span data-ttu-id="98f02-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f02-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="98f02-120">-ExportId</span></span>
<span data-ttu-id="98f02-121">Application Insights 연속 내보내기 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="98f02-122">-이름</span><span class="sxs-lookup"><span data-stu-id="98f02-122">-Name</span></span>
<span data-ttu-id="98f02-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="98f02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f02-124">-ResourceGroupName</span></span>
<span data-ttu-id="98f02-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="98f02-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f02-126">-ResourceId</span></span>
<span data-ttu-id="98f02-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="98f02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f02-128">CommonParameters</span></span>
<span data-ttu-id="98f02-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f02-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f02-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f02-131">입력</span><span class="sxs-lookup"><span data-stu-id="98f02-131">INPUTS</span></span>

### <span data-ttu-id="98f02-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="98f02-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="98f02-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98f02-133">System.String</span></span>

## <span data-ttu-id="98f02-134">출력</span><span class="sxs-lookup"><span data-stu-id="98f02-134">OUTPUTS</span></span>

### <span data-ttu-id="98f02-135">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="98f02-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="98f02-136">상속자</span><span class="sxs-lookup"><span data-stu-id="98f02-136">NOTES</span></span>

## <span data-ttu-id="98f02-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98f02-137">RELATED LINKS</span></span>