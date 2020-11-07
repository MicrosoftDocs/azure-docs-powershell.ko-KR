---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: 94d3a23d3ce43c97594f53e092544d2bbdeb9a1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868770"
---
# <span data-ttu-id="2233a-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2233a-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="2233a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2233a-102">SYNOPSIS</span></span>
<span data-ttu-id="2233a-103">Data Factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="2233a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2233a-104">SYNTAX</span></span>

### <span data-ttu-id="2233a-105">BySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="2233a-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2233a-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="2233a-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2233a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2233a-107">DESCRIPTION</span></span>
<span data-ttu-id="2233a-108">Get-AzDataFactoryV2 cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="2233a-109">Data factory의 이름을 지정 하는 경우이 cmdlet은 해당 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="2233a-110">이름을 지정 하지 않으면이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="2233a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2233a-111">EXAMPLES</span></span>

### <span data-ttu-id="2233a-112">예제 1: 모든 데이터 팩토리 가져오기</span><span class="sxs-lookup"><span data-stu-id="2233a-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded
```

<span data-ttu-id="2233a-113">Azure 구독에서 모든 데이터 팩터리에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="2233a-114">예제 2: 특정 data factory 가져오기</span><span class="sxs-lookup"><span data-stu-id="2233a-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="2233a-115">이 명령은 ADF 라는 리소스 그룹에 대 한 구독에서 WikiADF 이라는 data factory에 대 한 정보를 표시 한 다음이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="2233a-116">후속 cmdlet에서 DataFactory 매개 변수를 지정 하 여 $DataFactory에 저장 된 data factory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="2233a-117">변수</span><span class="sxs-lookup"><span data-stu-id="2233a-117">PARAMETERS</span></span>

### <span data-ttu-id="2233a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2233a-118">-DefaultProfile</span></span>
<span data-ttu-id="2233a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2233a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2233a-120">-Name</span></span>
<span data-ttu-id="2233a-121">정보를 가져올 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2233a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2233a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2233a-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2233a-124">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2233a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2233a-125">CommonParameters</span></span>
<span data-ttu-id="2233a-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2233a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2233a-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2233a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2233a-128">입력</span><span class="sxs-lookup"><span data-stu-id="2233a-128">INPUTS</span></span>

### <span data-ttu-id="2233a-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2233a-129">System.String</span></span>

## <span data-ttu-id="2233a-130">출력</span><span class="sxs-lookup"><span data-stu-id="2233a-130">OUTPUTS</span></span>

### <span data-ttu-id="2233a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2233a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2233a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2233a-132">NOTES</span></span>
<span data-ttu-id="2233a-133">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="2233a-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2233a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2233a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2233a-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2233a-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="2233a-136">제거-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2233a-136">Remove-AzDataFactoryV2</span></span>]()
