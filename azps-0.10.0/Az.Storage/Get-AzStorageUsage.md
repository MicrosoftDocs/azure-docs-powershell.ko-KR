---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876279"
---
# <span data-ttu-id="20391-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="20391-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="20391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20391-102">SYNOPSIS</span></span>
<span data-ttu-id="20391-103">현재 구독의 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20391-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="20391-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20391-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20391-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20391-105">DESCRIPTION</span></span>
<span data-ttu-id="20391-106">**AzStorageUsage** cmdlet은 현재 구독에 대 한 Azure 저장소의 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20391-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="20391-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20391-107">EXAMPLES</span></span>

### <span data-ttu-id="20391-108">예제 1: 저장소 리소스 사용 현황 가져오기</span><span class="sxs-lookup"><span data-stu-id="20391-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="20391-109">이 명령은 현재 구독의 저장소 리소스 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20391-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="20391-110">변수</span><span class="sxs-lookup"><span data-stu-id="20391-110">PARAMETERS</span></span>

### <span data-ttu-id="20391-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20391-111">-DefaultProfile</span></span>
<span data-ttu-id="20391-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20391-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20391-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20391-113">CommonParameters</span></span>
<span data-ttu-id="20391-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20391-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20391-115">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20391-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20391-116">입력</span><span class="sxs-lookup"><span data-stu-id="20391-116">INPUTS</span></span>

### <span data-ttu-id="20391-117">않아야</span><span class="sxs-lookup"><span data-stu-id="20391-117">None</span></span>

## <span data-ttu-id="20391-118">출력</span><span class="sxs-lookup"><span data-stu-id="20391-118">OUTPUTS</span></span>

### <span data-ttu-id="20391-119">Microsoft. Azure. i m//. m a i 사용</span><span class="sxs-lookup"><span data-stu-id="20391-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="20391-120">상속자</span><span class="sxs-lookup"><span data-stu-id="20391-120">NOTES</span></span>

## <span data-ttu-id="20391-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20391-121">RELATED LINKS</span></span>

[<span data-ttu-id="20391-122">Azure 저장소 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="20391-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)

