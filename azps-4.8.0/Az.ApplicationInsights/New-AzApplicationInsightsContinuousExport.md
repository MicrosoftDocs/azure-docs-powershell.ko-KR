---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048521"
---
# <span data-ttu-id="4c39f-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="4c39f-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="4c39f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c39f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c39f-103">Application insights 리소스에 대 한 새 application insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4c39f-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="4c39f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c39f-104">SYNTAX</span></span>

### <span data-ttu-id="4c39f-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c39f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c39f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c39f-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c39f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c39f-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c39f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4c39f-108">DESCRIPTION</span></span>
<span data-ttu-id="4c39f-109">Application insights 리소스에 대 한 새 application insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4c39f-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="4c39f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4c39f-110">EXAMPLES</span></span>

### <span data-ttu-id="4c39f-111">예제 1 application insights 리소스에 대 한 새 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4c39f-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="4c39f-112">"요청" 및 "추적" 문서 유형을 저장소로 내보내기 위한 새 application insights 연속 내보내기 구성을 만듭니다. "teststorageaccount" 리소스 그룹의 "testcontainer" 저장소 계정에 "에서"를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="4c39f-113">SAS 토큰은 유효 해야 하 고 컨테이너에 대 한 쓰기 권한이 있어야 하며, 그렇지 않은 경우에는 연속 내보내기 기능이 작동 하지 않습니다. SAS 토큰이 만료 되 면 연속 내보내기 기능이 작동을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="4c39f-114">변수</span><span class="sxs-lookup"><span data-stu-id="4c39f-114">PARAMETERS</span></span>

### <span data-ttu-id="4c39f-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4c39f-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4c39f-116">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="4c39f-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4c39f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c39f-117">-DefaultProfile</span></span>
<span data-ttu-id="4c39f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c39f-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="4c39f-119">-DocumentType</span></span>
<span data-ttu-id="4c39f-120">내보내야 할 문서 형식</span><span class="sxs-lookup"><span data-stu-id="4c39f-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c39f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="4c39f-121">-Name</span></span>
<span data-ttu-id="4c39f-122">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-122">Component Name.</span></span>

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

### <span data-ttu-id="4c39f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c39f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c39f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c39f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c39f-125">-ResourceId</span></span>
<span data-ttu-id="4c39f-126">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4c39f-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4c39f-127">-StorageAccountId</span></span>
<span data-ttu-id="4c39f-128">대상 저장소 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="4c39f-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="4c39f-129">-StorageLocation</span></span>
<span data-ttu-id="4c39f-130">대상 저장소 위치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="4c39f-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="4c39f-131">-StorageSASUri</span></span>
<span data-ttu-id="4c39f-132">대상 저장소 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="4c39f-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4c39f-133">-Confirm</span></span>
<span data-ttu-id="4c39f-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c39f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c39f-135">-WhatIf</span></span>
<span data-ttu-id="4c39f-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c39f-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c39f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c39f-138">CommonParameters</span></span>
<span data-ttu-id="4c39f-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c39f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c39f-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c39f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c39f-141">입력</span><span class="sxs-lookup"><span data-stu-id="4c39f-141">INPUTS</span></span>

### <span data-ttu-id="4c39f-142">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4c39f-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="4c39f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4c39f-143">System.String</span></span>

## <span data-ttu-id="4c39f-144">출력</span><span class="sxs-lookup"><span data-stu-id="4c39f-144">OUTPUTS</span></span>

### <span data-ttu-id="4c39f-145">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4c39f-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="4c39f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4c39f-146">NOTES</span></span>

## <span data-ttu-id="4c39f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c39f-147">RELATED LINKS</span></span>