---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349389"
---
# <span data-ttu-id="aa6aa-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="aa6aa-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="aa6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6aa-103">목록 또는 지정된 API 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="aa6aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa6aa-104">SYNTAX</span></span>

### <span data-ttu-id="aa6aa-105">GetAllApiOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa6aa-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa6aa-106">GetById</span><span class="sxs-lookup"><span data-stu-id="aa6aa-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa6aa-107">설명</span><span class="sxs-lookup"><span data-stu-id="aa6aa-107">DESCRIPTION</span></span>
<span data-ttu-id="aa6aa-108">**Get-AzApiManagementOperation은** 목록 또는 지정된 API 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="aa6aa-109">예제</span><span class="sxs-lookup"><span data-stu-id="aa6aa-109">EXAMPLES</span></span>

### <span data-ttu-id="aa6aa-110">예제 1: 모든 API 관리 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="aa6aa-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="aa6aa-111">이 명령은 모든 API 관리 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="aa6aa-112">예제 2: 작업 ID로 API Management 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="aa6aa-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="aa6aa-113">이 명령은 Operation0003이라는 작업 ID로 API 관리 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="aa6aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa6aa-114">PARAMETERS</span></span>

### <span data-ttu-id="aa6aa-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa6aa-115">-ApiId</span></span>
<span data-ttu-id="aa6aa-116">API 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="aa6aa-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="aa6aa-117">-ApiRevision</span></span>
<span data-ttu-id="aa6aa-118">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-118">Identifier of API Revision.</span></span> <span data-ttu-id="aa6aa-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-119">This parameter is optional.</span></span> <span data-ttu-id="aa6aa-120">지정하지 않으면 현재 활성 API 개정에서 작업이 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="aa6aa-121">-Context</span><span class="sxs-lookup"><span data-stu-id="aa6aa-121">-Context</span></span>
<span data-ttu-id="aa6aa-122">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6aa-123">-DefaultProfile</span></span>
<span data-ttu-id="aa6aa-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa6aa-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="aa6aa-125">-OperationId</span></span>
<span data-ttu-id="aa6aa-126">작업 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6aa-127">CommonParameters</span></span>
<span data-ttu-id="aa6aa-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6aa-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa6aa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6aa-130">입력</span><span class="sxs-lookup"><span data-stu-id="aa6aa-130">INPUTS</span></span>

### <span data-ttu-id="aa6aa-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa6aa-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa6aa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aa6aa-132">System.String</span></span>

## <span data-ttu-id="aa6aa-133">출력</span><span class="sxs-lookup"><span data-stu-id="aa6aa-133">OUTPUTS</span></span>

### <span data-ttu-id="aa6aa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="aa6aa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="aa6aa-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa6aa-135">NOTES</span></span>

## <span data-ttu-id="aa6aa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa6aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa6aa-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="aa6aa-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="aa6aa-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="aa6aa-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="aa6aa-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="aa6aa-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)

