---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869338"
---
# <span data-ttu-id="5ba91-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="5ba91-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="5ba91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba91-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba91-103">API Management로 거를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="5ba91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ba91-104">SYNTAX</span></span>

### <span data-ttu-id="5ba91-105">EventHubLoggerSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ba91-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba91-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="5ba91-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba91-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5ba91-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba91-108">**Set-AzApiManagementLogger** Cmdlet은 Azure API Management **로 거** 의 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="5ba91-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5ba91-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba91-110">예제 1: EventHub로 거 수정</span><span class="sxs-lookup"><span data-stu-id="5ba91-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="5ba91-111">이 명령은 ID Logger123 인로 거를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="5ba91-112">변수</span><span class="sxs-lookup"><span data-stu-id="5ba91-112">PARAMETERS</span></span>

### <span data-ttu-id="5ba91-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5ba91-113">-ConnectionString</span></span>
<span data-ttu-id="5ba91-114">정책 보내기 권한이 포함 된 Azure 이벤트 허브 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5ba91-115">-Context</span></span>
<span data-ttu-id="5ba91-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba91-117">-DefaultProfile</span></span>
<span data-ttu-id="5ba91-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba91-119">-설명</span><span class="sxs-lookup"><span data-stu-id="5ba91-119">-Description</span></span>
<span data-ttu-id="5ba91-120">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="5ba91-121">-InstrumentationKey</span></span>
<span data-ttu-id="5ba91-122">Application Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="5ba91-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="5ba91-124">-IsBuffered</span></span>
<span data-ttu-id="5ba91-125">게시 하기 전에로 거의 레코드를 버퍼링 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="5ba91-126">레코드가 버퍼링 되 면 15 초 마다 이벤트 허브에 또는 버퍼가 256 KB의 메시지를 받을 때마다 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="5ba91-127">-LoggerId</span></span>
<span data-ttu-id="5ba91-128">업데이트할로 거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="5ba91-129">-이름</span><span class="sxs-lookup"><span data-stu-id="5ba91-129">-Name</span></span>
<span data-ttu-id="5ba91-130">Azure 클래식 포털에서 이벤트 허브의 엔터티 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ba91-131">-PassThru</span></span>
<span data-ttu-id="5ba91-132">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementLogger** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba91-133">CommonParameters</span></span>
<span data-ttu-id="5ba91-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba91-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba91-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba91-136">입력</span><span class="sxs-lookup"><span data-stu-id="5ba91-136">INPUTS</span></span>

### <span data-ttu-id="5ba91-137">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5ba91-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5ba91-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ba91-138">System.String</span></span>

### <span data-ttu-id="5ba91-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ba91-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ba91-140">출력</span><span class="sxs-lookup"><span data-stu-id="5ba91-140">OUTPUTS</span></span>

### <span data-ttu-id="5ba91-141">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="5ba91-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="5ba91-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5ba91-142">NOTES</span></span>

## <span data-ttu-id="5ba91-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ba91-143">RELATED LINKS</span></span>

[<span data-ttu-id="5ba91-144">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="5ba91-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="5ba91-145">새로운 AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="5ba91-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="5ba91-146">제거-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="5ba91-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

