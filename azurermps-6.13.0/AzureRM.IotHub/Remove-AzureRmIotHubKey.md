---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527940"
---
# <span data-ttu-id="41c88-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="41c88-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="41c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41c88-102">SYNOPSIS</span></span>
<span data-ttu-id="41c88-103">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41c88-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41c88-105">DESCRIPTION</span></span>
<span data-ttu-id="41c88-106">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="41c88-107">이름이 같은 키가 여러 개 있는 경우 목록의 첫 번째 항목은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="41c88-108">예제의</span><span class="sxs-lookup"><span data-stu-id="41c88-108">EXAMPLES</span></span>

### <span data-ttu-id="41c88-109">예제 1 IotHub 삭제</span><span class="sxs-lookup"><span data-stu-id="41c88-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="41c88-110">"Myiothub" 이라는 IotHub에서 iothubowner1 이라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="41c88-111">변수</span><span class="sxs-lookup"><span data-stu-id="41c88-111">PARAMETERS</span></span>

### <span data-ttu-id="41c88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c88-112">-DefaultProfile</span></span>
<span data-ttu-id="41c88-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="41c88-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41c88-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="41c88-114">-KeyName</span></span>
<span data-ttu-id="41c88-115">키 이름</span><span class="sxs-lookup"><span data-stu-id="41c88-115">Name of the Key</span></span>

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

### <span data-ttu-id="41c88-116">-이름</span><span class="sxs-lookup"><span data-stu-id="41c88-116">-Name</span></span>
<span data-ttu-id="41c88-117">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="41c88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c88-118">-ResourceGroupName</span></span>
<span data-ttu-id="41c88-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="41c88-119">Resource Group Name</span></span>

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

### <span data-ttu-id="41c88-120">-확인</span><span class="sxs-lookup"><span data-stu-id="41c88-120">-Confirm</span></span>
<span data-ttu-id="41c88-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c88-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c88-122">-WhatIf</span></span>
<span data-ttu-id="41c88-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c88-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c88-125">CommonParameters</span></span>
<span data-ttu-id="41c88-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c88-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c88-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c88-128">입력</span><span class="sxs-lookup"><span data-stu-id="41c88-128">INPUTS</span></span>

### <span data-ttu-id="41c88-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41c88-129">System.String</span></span>

## <span data-ttu-id="41c88-130">출력</span><span class="sxs-lookup"><span data-stu-id="41c88-130">OUTPUTS</span></span>

### <span data-ttu-id="41c88-131">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="41c88-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="41c88-132">상속자</span><span class="sxs-lookup"><span data-stu-id="41c88-132">NOTES</span></span>

## <span data-ttu-id="41c88-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41c88-133">RELATED LINKS</span></span>