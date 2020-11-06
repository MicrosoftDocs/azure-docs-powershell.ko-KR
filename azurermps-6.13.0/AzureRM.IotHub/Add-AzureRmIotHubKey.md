---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530283"
---
# <span data-ttu-id="56c92-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="56c92-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="56c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c92-102">SYNOPSIS</span></span>
<span data-ttu-id="56c92-103">IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56c92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56c92-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c92-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56c92-105">DESCRIPTION</span></span>
<span data-ttu-id="56c92-106">제공 된 IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="56c92-107">KeyNames은 고유 하지 않으므로 신중 하 게 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="56c92-108">예제의</span><span class="sxs-lookup"><span data-stu-id="56c92-108">EXAMPLES</span></span>

### <span data-ttu-id="56c92-109">예제 1 IotHub에 키 추가</span><span class="sxs-lookup"><span data-stu-id="56c92-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="56c92-110">RegistryRead 권한이 있는 iothub "myiothub"에 대해 "mykey" 라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="56c92-111">변수</span><span class="sxs-lookup"><span data-stu-id="56c92-111">PARAMETERS</span></span>

### <span data-ttu-id="56c92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-112">-DefaultProfile</span></span>
<span data-ttu-id="56c92-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56c92-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56c92-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="56c92-114">-KeyName</span></span>
<span data-ttu-id="56c92-115">키 이름</span><span class="sxs-lookup"><span data-stu-id="56c92-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c92-116">-이름</span><span class="sxs-lookup"><span data-stu-id="56c92-116">-Name</span></span>
<span data-ttu-id="56c92-117">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="56c92-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="56c92-118">-PrimaryKey</span></span>
<span data-ttu-id="56c92-119">기본 키</span><span class="sxs-lookup"><span data-stu-id="56c92-119">The primary key</span></span>

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

### <span data-ttu-id="56c92-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c92-120">-ResourceGroupName</span></span>
<span data-ttu-id="56c92-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="56c92-121">Resource Group Name</span></span>

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

### <span data-ttu-id="56c92-122">-권한</span><span class="sxs-lookup"><span data-stu-id="56c92-122">-Rights</span></span>
<span data-ttu-id="56c92-123">이 IOTHub에 대 한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="56c92-123">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c92-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="56c92-124">-SecondaryKey</span></span>
<span data-ttu-id="56c92-125">보조 키</span><span class="sxs-lookup"><span data-stu-id="56c92-125">The Secondary Key</span></span>

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

### <span data-ttu-id="56c92-126">-확인</span><span class="sxs-lookup"><span data-stu-id="56c92-126">-Confirm</span></span>
<span data-ttu-id="56c92-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c92-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c92-128">-WhatIf</span></span>
<span data-ttu-id="56c92-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c92-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c92-131">CommonParameters</span></span>
<span data-ttu-id="56c92-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c92-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c92-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c92-134">입력</span><span class="sxs-lookup"><span data-stu-id="56c92-134">INPUTS</span></span>

### <span data-ttu-id="56c92-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56c92-135">System.String</span></span>

## <span data-ttu-id="56c92-136">출력</span><span class="sxs-lookup"><span data-stu-id="56c92-136">OUTPUTS</span></span>

### <span data-ttu-id="56c92-137">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="56c92-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="56c92-138">상속자</span><span class="sxs-lookup"><span data-stu-id="56c92-138">NOTES</span></span>

## <span data-ttu-id="56c92-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56c92-139">RELATED LINKS</span></span>