---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204166"
---
# <span data-ttu-id="5a8da-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="5a8da-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="5a8da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a8da-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8da-103">웹 앱 슬롯 구성 이름 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a8da-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="5a8da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a8da-104">SYNTAX</span></span>

### <span data-ttu-id="5a8da-105">S1</span><span class="sxs-lookup"><span data-stu-id="5a8da-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a8da-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="5a8da-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a8da-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5a8da-107">DESCRIPTION</span></span>
<span data-ttu-id="5a8da-108">**AzWebAppSlotConfigName** cmdlet은 현재 슬롯 설정으로 표시 된 앱 설정 및 연결 문자열 이름 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8da-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="5a8da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5a8da-109">EXAMPLES</span></span>

### <span data-ttu-id="5a8da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5a8da-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5a8da-111">이 명령은 리소스 그룹 기본값과 연결 된 ContosoSite 이라는 웹 앱에 관련 된 앱 설정 및 연결 문자열을 가져옵니다. WestUS</span><span class="sxs-lookup"><span data-stu-id="5a8da-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5a8da-112">변수</span><span class="sxs-lookup"><span data-stu-id="5a8da-112">PARAMETERS</span></span>

### <span data-ttu-id="5a8da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8da-113">-DefaultProfile</span></span>
<span data-ttu-id="5a8da-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a8da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a8da-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5a8da-115">-Name</span></span>
<span data-ttu-id="5a8da-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="5a8da-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a8da-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a8da-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5a8da-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8da-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="5a8da-119">-WebApp</span></span>
<span data-ttu-id="5a8da-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="5a8da-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8da-121">CommonParameters</span></span>
<span data-ttu-id="5a8da-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8da-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a8da-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8da-124">입력</span><span class="sxs-lookup"><span data-stu-id="5a8da-124">INPUTS</span></span>

### <span data-ttu-id="5a8da-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a8da-125">System.String</span></span>

### <span data-ttu-id="5a8da-126">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="5a8da-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5a8da-127">출력</span><span class="sxs-lookup"><span data-stu-id="5a8da-127">OUTPUTS</span></span>

### <span data-ttu-id="5a8da-128">SlotConfigNamesResource/. m i.</span><span class="sxs-lookup"><span data-stu-id="5a8da-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="5a8da-129">상속자</span><span class="sxs-lookup"><span data-stu-id="5a8da-129">NOTES</span></span>

## <span data-ttu-id="5a8da-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a8da-130">RELATED LINKS</span></span>