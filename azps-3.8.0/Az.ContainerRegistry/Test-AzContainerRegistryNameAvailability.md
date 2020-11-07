---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877893"
---
# <span data-ttu-id="9adc4-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9adc4-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="9adc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adc4-102">SYNOPSIS</span></span>
<span data-ttu-id="9adc4-103">컨테이너 레지스트리 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adc4-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="9adc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9adc4-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9adc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9adc4-105">DESCRIPTION</span></span>
<span data-ttu-id="9adc4-106">Test-AzContainerRegistryNameAvailability cmdlet은 컨테이너 레지스트리 이름이 유효 하며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adc4-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="9adc4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9adc4-107">EXAMPLES</span></span>

### <span data-ttu-id="9adc4-108">예제 1: 컨테이너 레지스트리 이름의 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="9adc4-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="9adc4-109">이 명령은 컨테이너 레지스트리 이름 SomeRegistryName의 사용 가능 여부를 확인 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="9adc4-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="9adc4-110">변수</span><span class="sxs-lookup"><span data-stu-id="9adc4-110">PARAMETERS</span></span>

### <span data-ttu-id="9adc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adc4-111">-DefaultProfile</span></span>
<span data-ttu-id="9adc4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9adc4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9adc4-113">-이름</span><span class="sxs-lookup"><span data-stu-id="9adc4-113">-Name</span></span>
<span data-ttu-id="9adc4-114">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9adc4-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adc4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adc4-115">CommonParameters</span></span>
<span data-ttu-id="9adc4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adc4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adc4-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9adc4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adc4-118">입력</span><span class="sxs-lookup"><span data-stu-id="9adc4-118">INPUTS</span></span>

### <span data-ttu-id="9adc4-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9adc4-119">System.String</span></span>

## <span data-ttu-id="9adc4-120">출력</span><span class="sxs-lookup"><span data-stu-id="9adc4-120">OUTPUTS</span></span>

### <span data-ttu-id="9adc4-121">ContainerRegistry. RegistryNameStatus/.</span><span class="sxs-lookup"><span data-stu-id="9adc4-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="9adc4-122">상속자</span><span class="sxs-lookup"><span data-stu-id="9adc4-122">NOTES</span></span>

## <span data-ttu-id="9adc4-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9adc4-123">RELATED LINKS</span></span>

[<span data-ttu-id="9adc4-124">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9adc4-124">New-AzContainerRegistry</span></span>]()
