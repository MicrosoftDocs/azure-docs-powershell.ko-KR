---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048403"
---
# <span data-ttu-id="3521f-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="3521f-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="3521f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3521f-102">SYNOPSIS</span></span>
<span data-ttu-id="3521f-103">가상 머신에서 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3521f-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="3521f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3521f-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3521f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3521f-105">DESCRIPTION</span></span>

## <span data-ttu-id="3521f-106">예제의</span><span class="sxs-lookup"><span data-stu-id="3521f-106">EXAMPLES</span></span>

### <span data-ttu-id="3521f-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="3521f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3521f-108">변수</span><span class="sxs-lookup"><span data-stu-id="3521f-108">PARAMETERS</span></span>

### <span data-ttu-id="3521f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3521f-109">-DefaultProfile</span></span>
<span data-ttu-id="3521f-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3521f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3521f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3521f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3521f-112">태그</span><span class="sxs-lookup"><span data-stu-id="3521f-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3521f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="3521f-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3521f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3521f-114">CommonParameters</span></span>
<span data-ttu-id="3521f-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3521f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3521f-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3521f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3521f-117">입력</span><span class="sxs-lookup"><span data-stu-id="3521f-117">INPUTS</span></span>

### <span data-ttu-id="3521f-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3521f-118">System.String</span></span>

## <span data-ttu-id="3521f-119">출력</span><span class="sxs-lookup"><span data-stu-id="3521f-119">OUTPUTS</span></span>

### <span data-ttu-id="3521f-120">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="3521f-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3521f-121">상속자</span><span class="sxs-lookup"><span data-stu-id="3521f-121">NOTES</span></span>

## <span data-ttu-id="3521f-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3521f-122">RELATED LINKS</span></span>