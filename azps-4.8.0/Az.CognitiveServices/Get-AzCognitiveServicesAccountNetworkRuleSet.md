---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048155"
---
# <span data-ttu-id="6f46a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f46a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6f46a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f46a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f46a-103">인지 서비스 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f46a-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6f46a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f46a-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f46a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f46a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f46a-106">**AzCognitiveServicesAccountNetworkRuleSet** Cmdlet은 인지 서비스 계정의 networkrule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6f46a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f46a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f46a-108">예제 1: 지정 된 인식 서비스 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f46a-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="6f46a-109">이 명령은 지정 된 인식 서비스 계정의 NetworkRule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="6f46a-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f46a-110">PARAMETERS</span></span>

### <span data-ttu-id="6f46a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f46a-111">-DefaultProfile</span></span>
<span data-ttu-id="6f46a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f46a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="6f46a-113">-Name</span></span>
<span data-ttu-id="6f46a-114">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f46a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6f46a-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f46a-117">CommonParameters</span></span>
<span data-ttu-id="6f46a-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f46a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f46a-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f46a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f46a-120">입력</span><span class="sxs-lookup"><span data-stu-id="6f46a-120">INPUTS</span></span>

### <span data-ttu-id="6f46a-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f46a-121">System.String</span></span>

## <span data-ttu-id="6f46a-122">출력</span><span class="sxs-lookup"><span data-stu-id="6f46a-122">OUTPUTS</span></span>

### <span data-ttu-id="6f46a-123">CognitiveServices. a m m 네트워크 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="6f46a-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6f46a-124">상속자</span><span class="sxs-lookup"><span data-stu-id="6f46a-124">NOTES</span></span>

## <span data-ttu-id="6f46a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f46a-125">RELATED LINKS</span></span>