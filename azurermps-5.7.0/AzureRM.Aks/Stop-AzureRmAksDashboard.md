---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532883"
---
# <span data-ttu-id="04e0b-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="04e0b-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="04e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="04e0b-103">시작-AzureRmKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04e0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04e0b-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e0b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="04e0b-106">시작-AzureRmKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="04e0b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="04e0b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="04e0b-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="04e0b-109">시작-AzureRmKubernetesDashboard를 실행 하 여 기존 SSH 터널 설정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="04e0b-110">변수</span><span class="sxs-lookup"><span data-stu-id="04e0b-110">PARAMETERS</span></span>

### <span data-ttu-id="04e0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e0b-111">-DefaultProfile</span></span>
<span data-ttu-id="04e0b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e0b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04e0b-113">-PassThru</span></span>
<span data-ttu-id="04e0b-114">SSH 터널이 닫혀 있으면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04e0b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e0b-115">CommonParameters</span></span>
<span data-ttu-id="04e0b-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e0b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e0b-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e0b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e0b-118">입력</span><span class="sxs-lookup"><span data-stu-id="04e0b-118">INPUTS</span></span>

### <span data-ttu-id="04e0b-119">않아야</span><span class="sxs-lookup"><span data-stu-id="04e0b-119">None</span></span>

## <span data-ttu-id="04e0b-120">출력</span><span class="sxs-lookup"><span data-stu-id="04e0b-120">OUTPUTS</span></span>

### <span data-ttu-id="04e0b-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="04e0b-121">System.Boolean</span></span>

## <span data-ttu-id="04e0b-122">상속자</span><span class="sxs-lookup"><span data-stu-id="04e0b-122">NOTES</span></span>

## <span data-ttu-id="04e0b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04e0b-123">RELATED LINKS</span></span>