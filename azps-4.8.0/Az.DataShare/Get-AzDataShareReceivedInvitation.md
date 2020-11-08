---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214570"
---
# <span data-ttu-id="ce9e6-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="ce9e6-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="ce9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9e6-103">소비자 초대에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="ce9e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce9e6-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9e6-106">**AzDataShareReceivedInvitation** cmdlet은 소비자가 receieved 하는 모든 초대에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="ce9e6-107">위치 또는 초대 id를 제공 하는 경우이 cmdlet은 특정 위치의 초대 또는 초대 id를 포함 하는 방법에 대 한 정보를 제공 합니다. 그렇지 않으면 소비자에 게 전송 되는 초대 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="ce9e6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ce9e6-108">EXAMPLES</span></span>

### <span data-ttu-id="ce9e6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce9e6-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="ce9e6-110">이 commant는 소비자 초대에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="ce9e6-111">변수</span><span class="sxs-lookup"><span data-stu-id="ce9e6-111">PARAMETERS</span></span>

### <span data-ttu-id="ce9e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9e6-112">-DefaultProfile</span></span>
<span data-ttu-id="ce9e6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce9e6-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="ce9e6-114">-InvitationId</span></span>
<span data-ttu-id="ce9e6-115">Azure dataShare 초대 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9e6-116">-위치</span><span class="sxs-lookup"><span data-stu-id="ce9e6-116">-Location</span></span>
<span data-ttu-id="ce9e6-117">Azure data share 초대 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9e6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9e6-118">CommonParameters</span></span>
<span data-ttu-id="ce9e6-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9e6-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9e6-121">입력</span><span class="sxs-lookup"><span data-stu-id="ce9e6-121">INPUTS</span></span>

### <span data-ttu-id="ce9e6-122">않아야</span><span class="sxs-lookup"><span data-stu-id="ce9e6-122">None</span></span>

## <span data-ttu-id="ce9e6-123">출력</span><span class="sxs-lookup"><span data-stu-id="ce9e6-123">OUTPUTS</span></span>

### <span data-ttu-id="ce9e6-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ce9e6-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ce9e6-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ce9e6-125">NOTES</span></span>

## <span data-ttu-id="ce9e6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce9e6-126">RELATED LINKS</span></span>