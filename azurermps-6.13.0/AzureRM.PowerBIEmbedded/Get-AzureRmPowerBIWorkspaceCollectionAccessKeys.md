---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 61d71bebfd395b6856c93e0bc3642125437b5fe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530143"
---
# <span data-ttu-id="eb221-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="eb221-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="eb221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb221-102">SYNOPSIS</span></span>
<span data-ttu-id="eb221-103">Power BI workspace 컬렉션과 연결 된 현재 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb221-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb221-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb221-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb221-105">DESCRIPTION</span></span>
<span data-ttu-id="eb221-106">**AzureRmPowerBIWorkspaceCollectionAccessKeys** Cmdlet은 Power BI workspace 컬렉션과 연결 된 현재 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="eb221-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eb221-107">EXAMPLES</span></span>

### <span data-ttu-id="eb221-108">예제 1: 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="eb221-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="eb221-109">이 명령은 지정 된 리소스 그룹의 WCN11 이라는 작업 영역 컬렉션에 대 한 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="eb221-110">변수</span><span class="sxs-lookup"><span data-stu-id="eb221-110">PARAMETERS</span></span>

### <span data-ttu-id="eb221-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb221-111">-DefaultProfile</span></span>
<span data-ttu-id="eb221-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb221-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb221-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb221-113">-ResourceGroupName</span></span>
<span data-ttu-id="eb221-114">컬렉션의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="eb221-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="eb221-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="eb221-116">이 cmdlet이 작동 하는 Power BI 작업 영역 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb221-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb221-117">CommonParameters</span></span>
<span data-ttu-id="eb221-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb221-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb221-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb221-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb221-120">입력</span><span class="sxs-lookup"><span data-stu-id="eb221-120">INPUTS</span></span>

### <span data-ttu-id="eb221-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb221-121">System.String</span></span>

## <span data-ttu-id="eb221-122">출력</span><span class="sxs-lookup"><span data-stu-id="eb221-122">OUTPUTS</span></span>

### <span data-ttu-id="eb221-123">PSWorkspaceCollectionAccessKey. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="eb221-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="eb221-124">상속자</span><span class="sxs-lookup"><span data-stu-id="eb221-124">NOTES</span></span>

## <span data-ttu-id="eb221-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb221-125">RELATED LINKS</span></span>

[<span data-ttu-id="eb221-126">다시 설정-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="eb221-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)

