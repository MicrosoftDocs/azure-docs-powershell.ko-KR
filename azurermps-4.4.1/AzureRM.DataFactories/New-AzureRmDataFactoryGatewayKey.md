---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530789"
---
# <span data-ttu-id="30aa5-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="30aa5-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="30aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="30aa5-103">Azure Data Factory에 대 한 게이트웨이 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="30aa5-104">이 cmdlet은 더 이상 사용 되지 않으며, 대신 **New-AzureRmDataFactoryGatewayAuthKey** 를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30aa5-105">구문과</span><span class="sxs-lookup"><span data-stu-id="30aa5-105">SYNTAX</span></span>

### <span data-ttu-id="30aa5-106">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="30aa5-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30aa5-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="30aa5-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30aa5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="30aa5-108">DESCRIPTION</span></span>
<span data-ttu-id="30aa5-109">**AzureRmDataFactoryGatewayKey** cmdlet은 지정 된 Azure Data Factory 게이트웨이에 대 한 게이트웨이 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="30aa5-110">이 키를 사용 하 여 클라우드 서비스에 게이트웨이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="30aa5-111">이 cmdlet은 더 이상 사용 되지 않으며, 대신 **New-AzureRmDataFactoryGatewayAuthKey** 를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="30aa5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="30aa5-112">EXAMPLES</span></span>

### <span data-ttu-id="30aa5-113">예제 1: 게이트웨이 키 만들기</span><span class="sxs-lookup"><span data-stu-id="30aa5-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="30aa5-114">이 명령은 ContosoGateway 이라는 data factory 게이트웨이에 대 한 게이트웨이 키를 만든 다음 파이프라인 연산자를 사용 하 여 게이트웨이 키를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="30aa5-115">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="30aa5-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="30aa5-116">변수</span><span class="sxs-lookup"><span data-stu-id="30aa5-116">PARAMETERS</span></span>

### <span data-ttu-id="30aa5-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="30aa5-117">-DataFactory</span></span>
<span data-ttu-id="30aa5-118">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="30aa5-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 게이트웨이 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30aa5-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="30aa5-120">-DataFactoryName</span></span>
<span data-ttu-id="30aa5-121">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="30aa5-122">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 게이트웨이 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30aa5-123">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="30aa5-123">-GatewayName</span></span>
<span data-ttu-id="30aa5-124">게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="30aa5-125">이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이에 대 한 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30aa5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30aa5-126">-ResourceGroupName</span></span>
<span data-ttu-id="30aa5-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="30aa5-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이에 대 한 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="30aa5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30aa5-129">-DefaultProfile</span></span>
<span data-ttu-id="30aa5-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30aa5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30aa5-131">CommonParameters</span></span>
<span data-ttu-id="30aa5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30aa5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30aa5-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30aa5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30aa5-134">입력</span><span class="sxs-lookup"><span data-stu-id="30aa5-134">INPUTS</span></span>

## <span data-ttu-id="30aa5-135">출력</span><span class="sxs-lookup"><span data-stu-id="30aa5-135">OUTPUTS</span></span>

### <span data-ttu-id="30aa5-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="30aa5-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="30aa5-137">상속자</span><span class="sxs-lookup"><span data-stu-id="30aa5-137">NOTES</span></span>
* <span data-ttu-id="30aa5-138">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="30aa5-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="30aa5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30aa5-139">RELATED LINKS</span></span>

<span data-ttu-id="30aa5-140">[새로운 AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [새로운 AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="30aa5-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

