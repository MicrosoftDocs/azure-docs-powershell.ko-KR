---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872725"
---
# <span data-ttu-id="b2267-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b2267-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="b2267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2267-102">SYNOPSIS</span></span>
<span data-ttu-id="b2267-103">복구 서비스 자격 증명 모음에 등록 된 ASR recovery services 공급자의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="b2267-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2267-104">SYNTAX</span></span>

### <span data-ttu-id="b2267-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2267-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2267-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b2267-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2267-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2267-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2267-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b2267-108">DESCRIPTION</span></span>
<span data-ttu-id="b2267-109">**AzRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음의 Azure Site Recovery 공급자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="b2267-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b2267-110">EXAMPLES</span></span>

### <span data-ttu-id="b2267-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2267-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="b2267-112">지정 된 패브릭에 해당 하는 복구 서비스 자격 증명 모음에 등록 된 모든 ASR 복제 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="b2267-113">변수</span><span class="sxs-lookup"><span data-stu-id="b2267-113">PARAMETERS</span></span>

### <span data-ttu-id="b2267-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2267-114">-DefaultProfile</span></span>
<span data-ttu-id="b2267-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b2267-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="b2267-116">-Fabric</span></span>
<span data-ttu-id="b2267-117">ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2267-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2267-118">-FriendlyName</span></span>
<span data-ttu-id="b2267-119">세부 정보를 얻을 ASR recovery services 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2267-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b2267-120">-Name</span></span>
<span data-ttu-id="b2267-121">세부 정보를 얻을 ASR recovery services 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2267-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2267-122">CommonParameters</span></span>
<span data-ttu-id="b2267-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2267-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2267-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2267-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2267-125">입력</span><span class="sxs-lookup"><span data-stu-id="b2267-125">INPUTS</span></span>

### <span data-ttu-id="b2267-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="b2267-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b2267-127">출력</span><span class="sxs-lookup"><span data-stu-id="b2267-127">OUTPUTS</span></span>

### <span data-ttu-id="b2267-128">SiteRecovery. r m/RecoveryServices 공급자</span><span class="sxs-lookup"><span data-stu-id="b2267-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="b2267-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b2267-129">NOTES</span></span>

## <span data-ttu-id="b2267-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2267-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2267-131">제거-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b2267-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="b2267-132">업데이트-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b2267-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)