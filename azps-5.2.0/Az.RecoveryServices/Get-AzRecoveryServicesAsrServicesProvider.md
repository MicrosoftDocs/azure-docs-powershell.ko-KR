---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5ede0387f5aabb1a4f4c4814f8090e0feeda2bf2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352593"
---
# <span data-ttu-id="09acc-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="09acc-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="09acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09acc-102">SYNOPSIS</span></span>
<span data-ttu-id="09acc-103">Recovery Services 자격 증명 모음에 등록된 ASR 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="09acc-104">구문</span><span class="sxs-lookup"><span data-stu-id="09acc-104">SYNTAX</span></span>

### <span data-ttu-id="09acc-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="09acc-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09acc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="09acc-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09acc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="09acc-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09acc-108">설명</span><span class="sxs-lookup"><span data-stu-id="09acc-108">DESCRIPTION</span></span>
<span data-ttu-id="09acc-109">**Get-AzRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음의 Azure Site Recovery 공급자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="09acc-110">예제</span><span class="sxs-lookup"><span data-stu-id="09acc-110">EXAMPLES</span></span>

### <span data-ttu-id="09acc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="09acc-111">Example 1</span></span>
```powershell
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="09acc-112">지정된 패브릭에 해당하는 Recovery Services 자격 증명 모음에 등록된 모든 ASR 복제 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

### <span data-ttu-id="09acc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="09acc-113">Example 2</span></span>

<span data-ttu-id="09acc-114">Recovery Services 자격 증명 모음에 등록된 ASR 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-114">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span> <span data-ttu-id="09acc-115">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="09acc-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrServicesProvider -Fabric $Fabric
```

## <span data-ttu-id="09acc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09acc-116">PARAMETERS</span></span>

### <span data-ttu-id="09acc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09acc-117">-DefaultProfile</span></span>
<span data-ttu-id="09acc-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="09acc-119">-Fabric</span><span class="sxs-lookup"><span data-stu-id="09acc-119">-Fabric</span></span>
<span data-ttu-id="09acc-120">ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-120">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="09acc-121">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="09acc-121">-FriendlyName</span></span>
<span data-ttu-id="09acc-122">세부 정보를 얻을 ASR 복구 서비스 공급자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-122">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="09acc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="09acc-123">-Name</span></span>
<span data-ttu-id="09acc-124">세부 정보를 얻을 ASR 복구 서비스 공급자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-124">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="09acc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09acc-125">CommonParameters</span></span>
<span data-ttu-id="09acc-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09acc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09acc-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09acc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09acc-128">입력</span><span class="sxs-lookup"><span data-stu-id="09acc-128">INPUTS</span></span>

### <span data-ttu-id="09acc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="09acc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="09acc-130">출력</span><span class="sxs-lookup"><span data-stu-id="09acc-130">OUTPUTS</span></span>

### <span data-ttu-id="09acc-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="09acc-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="09acc-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09acc-132">NOTES</span></span>

## <span data-ttu-id="09acc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09acc-133">RELATED LINKS</span></span>

[<span data-ttu-id="09acc-134">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="09acc-134">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="09acc-135">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="09acc-135">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)