---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 19a10312046a4c52ed1fad29732347f719065b95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873509"
---
# <span data-ttu-id="9affc-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9affc-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9affc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9affc-102">SYNOPSIS</span></span>
<span data-ttu-id="9affc-103">Azure Site Recovery 복제 보호 항목의 복제를 중지 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="9affc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9affc-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9affc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9affc-105">DESCRIPTION</span></span>
<span data-ttu-id="9affc-106">**AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 Azure Site Recovery 복제 보호 항목의 복제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="9affc-107">이 작업을 수행 하면 보호 된 항목에 대 한 복제가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="9affc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9affc-108">EXAMPLES</span></span>

### <span data-ttu-id="9affc-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9affc-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="9affc-110">지정 된 복제 보호 항목에 대 한 복제 사용 안 함 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9affc-111">변수</span><span class="sxs-lookup"><span data-stu-id="9affc-111">PARAMETERS</span></span>

### <span data-ttu-id="9affc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9affc-112">-DefaultProfile</span></span>
<span data-ttu-id="9affc-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9affc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9affc-114">-Force</span></span>
<span data-ttu-id="9affc-115">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9affc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9affc-116">-InputObject</span></span>
<span data-ttu-id="9affc-117">Cmdlet에 대 한 입력 개체: 복제를 사용 하지 않도록 설정할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9affc-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9affc-118">-WaitForCompletion</span></span>
<span data-ttu-id="9affc-119">Cmdlet이 반환 하기 전에 작업이 완료 될 때까지 대기 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="9affc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="9affc-120">-Confirm</span></span>
<span data-ttu-id="9affc-121">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-121">Specify if confirmation is required.</span></span> <span data-ttu-id="9affc-122">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="9affc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9affc-123">-WhatIf</span></span>
<span data-ttu-id="9affc-124">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9affc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9affc-125">CommonParameters</span></span>
<span data-ttu-id="9affc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9affc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9affc-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9affc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9affc-128">입력</span><span class="sxs-lookup"><span data-stu-id="9affc-128">INPUTS</span></span>

### <span data-ttu-id="9affc-129">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="9affc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9affc-130">출력</span><span class="sxs-lookup"><span data-stu-id="9affc-130">OUTPUTS</span></span>

### <span data-ttu-id="9affc-131">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="9affc-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9affc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="9affc-132">NOTES</span></span>

## <span data-ttu-id="9affc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9affc-133">RELATED LINKS</span></span>

[<span data-ttu-id="9affc-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9affc-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9affc-135">새로운 AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9affc-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9affc-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9affc-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)