---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529959"
---
# <span data-ttu-id="5c681-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="5c681-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="5c681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c681-102">SYNOPSIS</span></span>
<span data-ttu-id="5c681-103">테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c681-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c681-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c681-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c681-105">DESCRIPTION</span></span>
<span data-ttu-id="5c681-106">**AzureRmApiManagementTenantGitAccess** cmdlet은 테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="5c681-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c681-107">EXAMPLES</span></span>

### <span data-ttu-id="5c681-108">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c681-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="5c681-109">이 명령은 지정 된 컨텍스트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="5c681-110">변수</span><span class="sxs-lookup"><span data-stu-id="5c681-110">PARAMETERS</span></span>

### <span data-ttu-id="5c681-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5c681-111">-Context</span></span>
<span data-ttu-id="5c681-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c681-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c681-113">-DefaultProfile</span></span>
<span data-ttu-id="5c681-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5c681-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c681-115">CommonParameters</span></span>
<span data-ttu-id="5c681-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c681-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c681-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c681-118">입력</span><span class="sxs-lookup"><span data-stu-id="5c681-118">INPUTS</span></span>

### <span data-ttu-id="5c681-119">않아야</span><span class="sxs-lookup"><span data-stu-id="5c681-119">None</span></span>
<span data-ttu-id="5c681-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c681-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c681-121">출력</span><span class="sxs-lookup"><span data-stu-id="5c681-121">OUTPUTS</span></span>

### <span data-ttu-id="5c681-122">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="5c681-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="5c681-123">상속자</span><span class="sxs-lookup"><span data-stu-id="5c681-123">NOTES</span></span>

## <span data-ttu-id="5c681-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c681-124">RELATED LINKS</span></span>
