---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056844"
---
# <span data-ttu-id="978bb-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="978bb-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="978bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978bb-102">SYNOPSIS</span></span>
<span data-ttu-id="978bb-103">그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-103">Adds a product to a group.</span></span>

## <span data-ttu-id="978bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="978bb-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="978bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="978bb-105">DESCRIPTION</span></span>
<span data-ttu-id="978bb-106">**Add-AzApiManagementProductToGroup** cmdlet은 기존 그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="978bb-107">즉,이 cmdlet은 그룹을 제품에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="978bb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="978bb-108">EXAMPLES</span></span>

### <span data-ttu-id="978bb-109">예제 1: 그룹에 제품 추가</span><span class="sxs-lookup"><span data-stu-id="978bb-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="978bb-110">이 명령은 기존 그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="978bb-111">변수</span><span class="sxs-lookup"><span data-stu-id="978bb-111">PARAMETERS</span></span>

### <span data-ttu-id="978bb-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="978bb-112">-Context</span></span>
<span data-ttu-id="978bb-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="978bb-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-114">This parameter is required.</span></span>

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

### <span data-ttu-id="978bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978bb-115">-DefaultProfile</span></span>
<span data-ttu-id="978bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="978bb-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="978bb-117">-GroupId</span></span>
<span data-ttu-id="978bb-118">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-118">Specifies the group ID.</span></span>
<span data-ttu-id="978bb-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-119">This parameter is required.</span></span>

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

### <span data-ttu-id="978bb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="978bb-120">-PassThru</span></span>
<span data-ttu-id="978bb-121">passthru</span><span class="sxs-lookup"><span data-stu-id="978bb-121">passthru</span></span>

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

### <span data-ttu-id="978bb-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="978bb-122">-ProductId</span></span>
<span data-ttu-id="978bb-123">제품 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-123">Specifies the product ID.</span></span>
<span data-ttu-id="978bb-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-124">This parameter is required.</span></span>

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

### <span data-ttu-id="978bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978bb-125">CommonParameters</span></span>
<span data-ttu-id="978bb-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="978bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978bb-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="978bb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978bb-128">입력</span><span class="sxs-lookup"><span data-stu-id="978bb-128">INPUTS</span></span>

### <span data-ttu-id="978bb-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="978bb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="978bb-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="978bb-130">System.String</span></span>

### <span data-ttu-id="978bb-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="978bb-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="978bb-132">출력</span><span class="sxs-lookup"><span data-stu-id="978bb-132">OUTPUTS</span></span>

### <span data-ttu-id="978bb-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="978bb-133">System.Boolean</span></span>

## <span data-ttu-id="978bb-134">상속자</span><span class="sxs-lookup"><span data-stu-id="978bb-134">NOTES</span></span>

## <span data-ttu-id="978bb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="978bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="978bb-136">제거-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="978bb-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)

