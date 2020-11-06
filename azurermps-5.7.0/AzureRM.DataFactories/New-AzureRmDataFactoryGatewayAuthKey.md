---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: cf7632cc88f55e010a3da3d9ba543c391bbcc214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525195"
---
# <span data-ttu-id="d7006-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="d7006-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="d7006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7006-102">SYNOPSIS</span></span>
<span data-ttu-id="d7006-103">Azure Data Factory 게이트웨이에 대 한 auth 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7006-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7006-104">SYNTAX</span></span>

### <span data-ttu-id="d7006-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7006-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7006-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7006-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7006-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d7006-107">DESCRIPTION</span></span>
<span data-ttu-id="d7006-108">**AzureRmDataFactoryGatewayAuthKey** cmdlet은 지정 된 Azure Data Factory 게이트웨이에 대 한 게이트웨이 인증 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="d7006-109">이 키를 사용 하 여 클라우드 서비스에 게이트웨이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="d7006-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d7006-110">EXAMPLES</span></span>

### <span data-ttu-id="d7006-111">예제 1: Key1에 대 한 게이트웨이 인증 키 만들기</span><span class="sxs-lookup"><span data-stu-id="d7006-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="d7006-112">이 명령은 MyGateway 라는 data factory 게이트웨이에 대 한 Key1의 게이트웨이 인증 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="d7006-113">변수</span><span class="sxs-lookup"><span data-stu-id="d7006-113">PARAMETERS</span></span>

### <span data-ttu-id="d7006-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d7006-114">-DataFactoryName</span></span>
<span data-ttu-id="d7006-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7006-116">-DefaultProfile</span></span>
<span data-ttu-id="d7006-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d7006-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-118">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="d7006-118">-GatewayName</span></span>
<span data-ttu-id="d7006-119">Data factory 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-119">The data factory gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7006-120">-InputObject</span></span>
<span data-ttu-id="d7006-121">Data factory 개체</span><span class="sxs-lookup"><span data-stu-id="d7006-121">The data factory object</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d7006-122">-KeyName</span></span>
<span data-ttu-id="d7006-123">다시 생성할 게이트웨이 인증 키 이름입니다 (' key1 ' 또는 ' a m m ').</span><span class="sxs-lookup"><span data-stu-id="d7006-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7006-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7006-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d7006-126">-Confirm</span></span>
<span data-ttu-id="d7006-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7006-128">-WhatIf</span></span>
<span data-ttu-id="d7006-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7006-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7006-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7006-131">CommonParameters</span></span>
<span data-ttu-id="d7006-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7006-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7006-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7006-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7006-134">입력</span><span class="sxs-lookup"><span data-stu-id="d7006-134">INPUTS</span></span>

### <span data-ttu-id="d7006-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d7006-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="d7006-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7006-136">System.String</span></span>

## <span data-ttu-id="d7006-137">출력</span><span class="sxs-lookup"><span data-stu-id="d7006-137">OUTPUTS</span></span>

### <span data-ttu-id="d7006-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="d7006-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="d7006-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d7006-139">NOTES</span></span>
* <span data-ttu-id="d7006-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d7006-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7006-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7006-141">RELATED LINKS</span></span>

<span data-ttu-id="d7006-142">[새로운 AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="d7006-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>
