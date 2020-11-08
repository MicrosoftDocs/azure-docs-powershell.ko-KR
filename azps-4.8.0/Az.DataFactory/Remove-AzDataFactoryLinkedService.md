---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212842"
---
# <span data-ttu-id="9d15d-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d15d-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="9d15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d15d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d15d-103">Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="9d15d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d15d-104">SYNTAX</span></span>

### <span data-ttu-id="9d15d-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9d15d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d15d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d15d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d15d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9d15d-107">DESCRIPTION</span></span>
<span data-ttu-id="9d15d-108">**AzDataFactoryLinkedService** Cmdlet은 Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="9d15d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9d15d-109">EXAMPLES</span></span>

### <span data-ttu-id="9d15d-110">예제 1: 연결 된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="9d15d-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9d15d-111">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceTest 라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="9d15d-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="9d15d-113">변수</span><span class="sxs-lookup"><span data-stu-id="9d15d-113">PARAMETERS</span></span>

### <span data-ttu-id="9d15d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9d15d-114">-DataFactory</span></span>
<span data-ttu-id="9d15d-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9d15d-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d15d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d15d-117">-DataFactoryName</span></span>
<span data-ttu-id="9d15d-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9d15d-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d15d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d15d-120">-DefaultProfile</span></span>
<span data-ttu-id="9d15d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d15d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d15d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9d15d-122">-Force</span></span>
<span data-ttu-id="9d15d-123">이 cmdlet이 확인을 묻지 않고 연결 된 서비스를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d15d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9d15d-124">-Name</span></span>
<span data-ttu-id="9d15d-125">제거할 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d15d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d15d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d15d-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9d15d-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d15d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="9d15d-129">-Confirm</span></span>
<span data-ttu-id="9d15d-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d15d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d15d-131">-WhatIf</span></span>
<span data-ttu-id="9d15d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d15d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d15d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d15d-134">CommonParameters</span></span>
<span data-ttu-id="9d15d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d15d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d15d-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d15d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d15d-137">입력</span><span class="sxs-lookup"><span data-stu-id="9d15d-137">INPUTS</span></span>

### <span data-ttu-id="9d15d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9d15d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9d15d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9d15d-139">System.String</span></span>

## <span data-ttu-id="9d15d-140">출력</span><span class="sxs-lookup"><span data-stu-id="9d15d-140">OUTPUTS</span></span>

### <span data-ttu-id="9d15d-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="9d15d-141">System.Void</span></span>

## <span data-ttu-id="9d15d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9d15d-142">NOTES</span></span>
* <span data-ttu-id="9d15d-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="9d15d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9d15d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d15d-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d15d-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d15d-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="9d15d-146">새로운 AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d15d-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

