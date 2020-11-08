---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212673"
---
# <span data-ttu-id="120eb-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="120eb-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="120eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120eb-102">SYNOPSIS</span></span>
<span data-ttu-id="120eb-103">API 스키마에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="120eb-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="120eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="120eb-104">SYNTAX</span></span>

### <span data-ttu-id="120eb-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="120eb-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="120eb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="120eb-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="120eb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="120eb-107">DESCRIPTION</span></span>
<span data-ttu-id="120eb-108">**AzApiManagementApiSchema** CMDLET은 API 스키마의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="120eb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="120eb-109">EXAMPLES</span></span>

### <span data-ttu-id="120eb-110">예제 1: Api의 모든 Api 스키마에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="120eb-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="120eb-111">이 명령은 `swagger-petstore-extensive` 특정 ApiManagement 컨텍스트에 대 한 api와 연결 된 모든 api 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="120eb-112">예제 2: Api와 연결 된 특정 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="120eb-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="120eb-113">이 명령은 `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` 특정 ApiManagement 컨텍스트에 대 한 api와 연결 된 api 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="120eb-114">변수</span><span class="sxs-lookup"><span data-stu-id="120eb-114">PARAMETERS</span></span>

### <span data-ttu-id="120eb-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="120eb-115">-ApiId</span></span>
<span data-ttu-id="120eb-116">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-116">API identifier to look for.</span></span>
<span data-ttu-id="120eb-117">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120eb-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="120eb-118">-Context</span></span>
<span data-ttu-id="120eb-119">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="120eb-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120eb-121">-DefaultProfile</span></span>
<span data-ttu-id="120eb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="120eb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="120eb-123">-ResourceId</span></span>
<span data-ttu-id="120eb-124">Api 스키마의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="120eb-125">지정 된 경우 식별자를 사용 하 여 api 스키마를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="120eb-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-126">This parameter is required.</span></span>

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

### <span data-ttu-id="120eb-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="120eb-127">-SchemaId</span></span>
<span data-ttu-id="120eb-128">스키마의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120eb-129">CommonParameters</span></span>
<span data-ttu-id="120eb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="120eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120eb-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="120eb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120eb-132">입력</span><span class="sxs-lookup"><span data-stu-id="120eb-132">INPUTS</span></span>

### <span data-ttu-id="120eb-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="120eb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="120eb-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="120eb-134">System.String</span></span>

## <span data-ttu-id="120eb-135">출력</span><span class="sxs-lookup"><span data-stu-id="120eb-135">OUTPUTS</span></span>

### <span data-ttu-id="120eb-136">ApiManagement. ServiceManagement. \ PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="120eb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="120eb-137">상속자</span><span class="sxs-lookup"><span data-stu-id="120eb-137">NOTES</span></span>

## <span data-ttu-id="120eb-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="120eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="120eb-139">새로운 AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="120eb-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="120eb-140">제거-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="120eb-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="120eb-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="120eb-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)