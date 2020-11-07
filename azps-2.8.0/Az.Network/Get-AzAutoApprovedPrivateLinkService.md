---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 49fad6adf339afb9dacd6f916cf0abb8e6bb3728
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870241"
---
# <span data-ttu-id="7ad65-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad65-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7ad65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad65-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad65-103">자동 승인 된 개인 끝점에 연결할 수 있는 개인 링크 서비스 id의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ad65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ad65-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ad65-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7ad65-105">DESCRIPTION</span></span>
<span data-ttu-id="7ad65-106">**Get-AzAutoApprovedPrivateLinkService** 는 자동 승인 된 개인 끝점에 연결할 수 있는 개인 링크 서비스 id의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ad65-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7ad65-107">EXAMPLES</span></span>

### <span data-ttu-id="7ad65-108">예</span><span class="sxs-lookup"><span data-stu-id="7ad65-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7ad65-109">이 예제에서는 자동 승인 된 개인 끝점에 연결할 수 있는 개인 링크 서비스 id의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ad65-110">변수</span><span class="sxs-lookup"><span data-stu-id="7ad65-110">PARAMETERS</span></span>

### <span data-ttu-id="7ad65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad65-111">-DefaultProfile</span></span>
<span data-ttu-id="7ad65-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ad65-113">-위치</span><span class="sxs-lookup"><span data-stu-id="7ad65-113">-Location</span></span>
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

### <span data-ttu-id="7ad65-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad65-114">-ResourceGroupName</span></span>
<span data-ttu-id="7ad65-115">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7ad65-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad65-116">CommonParameters</span></span>
<span data-ttu-id="7ad65-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ad65-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad65-118">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ad65-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad65-119">입력</span><span class="sxs-lookup"><span data-stu-id="7ad65-119">INPUTS</span></span>

### <span data-ttu-id="7ad65-120">않아야</span><span class="sxs-lookup"><span data-stu-id="7ad65-120">None</span></span>

## <span data-ttu-id="7ad65-121">출력</span><span class="sxs-lookup"><span data-stu-id="7ad65-121">OUTPUTS</span></span>

### <span data-ttu-id="7ad65-122">PSAutoApprovedPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7ad65-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7ad65-123">상속자</span><span class="sxs-lookup"><span data-stu-id="7ad65-123">NOTES</span></span>

## <span data-ttu-id="7ad65-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ad65-124">RELATED LINKS</span></span>