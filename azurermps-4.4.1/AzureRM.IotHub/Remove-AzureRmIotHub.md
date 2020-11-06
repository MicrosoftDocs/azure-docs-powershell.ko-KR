---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534056"
---
# <span data-ttu-id="a2b3c-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="a2b3c-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="a2b3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b3c-103">IotHub를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2b3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2b3c-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b3c-106">IotHub를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="a2b3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2b3c-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b3c-108">예제 1 IotHub 제거</span><span class="sxs-lookup"><span data-stu-id="a2b3c-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a2b3c-109">"Myiothub" 이라는 IotHub를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="a2b3c-110">변수</span><span class="sxs-lookup"><span data-stu-id="a2b3c-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b3c-111">-이름</span><span class="sxs-lookup"><span data-stu-id="a2b3c-111">-Name</span></span>
<span data-ttu-id="a2b3c-112">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="a2b3c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b3c-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2b3c-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a2b3c-114">Resource Group Name</span></span>

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

### <span data-ttu-id="a2b3c-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a2b3c-115">-Confirm</span></span>
<span data-ttu-id="a2b3c-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b3c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b3c-117">-WhatIf</span></span>
<span data-ttu-id="a2b3c-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b3c-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b3c-120">-DefaultProfile</span></span>
<span data-ttu-id="a2b3c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b3c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b3c-122">CommonParameters</span></span>
<span data-ttu-id="a2b3c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b3c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b3c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b3c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b3c-125">입력</span><span class="sxs-lookup"><span data-stu-id="a2b3c-125">INPUTS</span></span>

### <span data-ttu-id="a2b3c-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2b3c-126">System.String</span></span>

## <span data-ttu-id="a2b3c-127">출력</span><span class="sxs-lookup"><span data-stu-id="a2b3c-127">OUTPUTS</span></span>

### <span data-ttu-id="a2b3c-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a2b3c-128">System.Object</span></span>

## <span data-ttu-id="a2b3c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a2b3c-129">NOTES</span></span>

## <span data-ttu-id="a2b3c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2b3c-130">RELATED LINKS</span></span>
