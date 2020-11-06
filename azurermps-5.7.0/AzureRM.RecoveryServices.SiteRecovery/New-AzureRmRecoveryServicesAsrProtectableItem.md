---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534736"
---
# <span data-ttu-id="2b267-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2b267-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="2b267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b267-102">SYNOPSIS</span></span>
<span data-ttu-id="2b267-103">보호 가능한 항목 목록에 실제 서버를 추가 (검색) 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b267-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b267-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b267-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b267-105">DESCRIPTION</span></span>
<span data-ttu-id="2b267-106">**AzureRmRecoveryServicesAsrProtectableItem** 는 ASR 패브릭 내의 보호 컨테이너에 있는 발견 된 보안 가능한 항목 목록에 보호 가능한 새 항목을 추가 합니다 (VMware 패브릭 유형에만 해당).</span><span class="sxs-lookup"><span data-stu-id="2b267-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="2b267-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b267-107">EXAMPLES</span></span>

### <span data-ttu-id="2b267-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b267-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="2b267-109">새 Azure Recovery Service ProtectableItem를 추가 하거나 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="2b267-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b267-110">PARAMETERS</span></span>

### <span data-ttu-id="2b267-111">-확인</span><span class="sxs-lookup"><span data-stu-id="2b267-111">-Confirm</span></span>
<span data-ttu-id="2b267-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-112">Prompt for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b267-113">-DefaultProfile</span></span>
<span data-ttu-id="2b267-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b267-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b267-115">-FriendlyName</span></span>
<span data-ttu-id="2b267-116">보호 가능한 항목의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-116">Friendly name for the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="2b267-117">-IPAddress</span></span>
<span data-ttu-id="2b267-118">보호 가능한 항목의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-118">IP address of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="2b267-119">-OSType</span></span>
<span data-ttu-id="2b267-120">보호 가능한 항목의 운영 체제 유형 (Windows/Linux)입니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2b267-121">-ProtectionContainer</span></span>
<span data-ttu-id="2b267-122">보호 가능한 항목을 추가 해야 하는 ASR 보호 컨테이너 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b267-123">-WhatIf</span></span>
<span data-ttu-id="2b267-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b267-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b267-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b267-126">CommonParameters</span></span>
<span data-ttu-id="2b267-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b267-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b267-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b267-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b267-129">입력</span><span class="sxs-lookup"><span data-stu-id="2b267-129">INPUTS</span></span>

### <span data-ttu-id="2b267-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="2b267-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2b267-131">출력</span><span class="sxs-lookup"><span data-stu-id="2b267-131">OUTPUTS</span></span>

### <span data-ttu-id="2b267-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="2b267-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b267-133">상속자</span><span class="sxs-lookup"><span data-stu-id="2b267-133">NOTES</span></span>

## <span data-ttu-id="2b267-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b267-134">RELATED LINKS</span></span>