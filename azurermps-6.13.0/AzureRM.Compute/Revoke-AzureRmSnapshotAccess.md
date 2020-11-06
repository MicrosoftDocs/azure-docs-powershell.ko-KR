---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524539"
---
# <span data-ttu-id="de3aa-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="de3aa-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="de3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="de3aa-103">스냅숏에 대 한 액세스 권한을 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de3aa-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="de3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="de3aa-106">AzureRmSnapshotAccess cmdlet은 스냅숏에 대 한 액세스 권한을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="de3aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="de3aa-107">EXAMPLES</span></span>

### <span data-ttu-id="de3aa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="de3aa-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="de3aa-109">리소스 그룹 ' ResourceGroup01 '에서 ' Snapshot01 ' 이라는 스냅숏에 대 한 액세스 권한을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="de3aa-110">변수</span><span class="sxs-lookup"><span data-stu-id="de3aa-110">PARAMETERS</span></span>

### <span data-ttu-id="de3aa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de3aa-111">-AsJob</span></span>
<span data-ttu-id="de3aa-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="de3aa-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3aa-113">-DefaultProfile</span></span>
<span data-ttu-id="de3aa-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="de3aa-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3aa-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="de3aa-117">-SnapshotName</span></span>
<span data-ttu-id="de3aa-118">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3aa-119">-확인</span><span class="sxs-lookup"><span data-stu-id="de3aa-119">-Confirm</span></span>
<span data-ttu-id="de3aa-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3aa-121">-WhatIf</span></span>
<span data-ttu-id="de3aa-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3aa-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3aa-124">CommonParameters</span></span>
<span data-ttu-id="de3aa-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3aa-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3aa-127">입력</span><span class="sxs-lookup"><span data-stu-id="de3aa-127">INPUTS</span></span>

### <span data-ttu-id="de3aa-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de3aa-128">System.String</span></span>

## <span data-ttu-id="de3aa-129">출력</span><span class="sxs-lookup"><span data-stu-id="de3aa-129">OUTPUTS</span></span>

### <span data-ttu-id="de3aa-130">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="de3aa-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="de3aa-131">상속자</span><span class="sxs-lookup"><span data-stu-id="de3aa-131">NOTES</span></span>

## <span data-ttu-id="de3aa-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de3aa-132">RELATED LINKS</span></span>