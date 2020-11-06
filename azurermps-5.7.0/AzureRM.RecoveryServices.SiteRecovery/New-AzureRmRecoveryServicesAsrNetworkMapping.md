---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531686"
---
# <span data-ttu-id="59835-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="59835-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="59835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59835-102">SYNOPSIS</span></span>
<span data-ttu-id="59835-103">두 네트워크 간에 ASR 네트워크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59835-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59835-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59835-104">SYNTAX</span></span>

### <span data-ttu-id="59835-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="59835-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59835-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="59835-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59835-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="59835-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59835-108">설명은</span><span class="sxs-lookup"><span data-stu-id="59835-108">DESCRIPTION</span></span>
<span data-ttu-id="59835-109">**AzureRmRecoveryServicesAsrNetworkMapping** cmdlet은 두 네트워크 간에 asr 네트워크 매핑을 만드는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 asr 작업의 asr 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="59835-110">예제의</span><span class="sxs-lookup"><span data-stu-id="59835-110">EXAMPLES</span></span>

### <span data-ttu-id="59835-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="59835-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="59835-112">지정 된 이름, 기본 및 복구 네트워크를 사용 하 여 네트워크 매핑 만들기 작업을 시작 하 고 작업을 추적 하는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="59835-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="59835-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="59835-114">지정 된 이름, 기본 및 복구 네트워크를 사용 하 여 만들기 작업을 위해 네트워크 매핑을 시작 하 고 작업을 추적 하는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="59835-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="59835-115">변수</span><span class="sxs-lookup"><span data-stu-id="59835-115">PARAMETERS</span></span>

### <span data-ttu-id="59835-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="59835-116">-AzureToAzure</span></span>
<span data-ttu-id="59835-117">생성 되는 네트워크 매핑이 두 Azure 지역 간에 Azure 가상 컴퓨터를 복제 하는 데 사용 되도록 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="59835-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-118">-확인</span><span class="sxs-lookup"><span data-stu-id="59835-118">-Confirm</span></span>
<span data-ttu-id="59835-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59835-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59835-120">-DefaultProfile</span></span>
<span data-ttu-id="59835-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59835-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="59835-122">-이름</span><span class="sxs-lookup"><span data-stu-id="59835-122">-Name</span></span>
<span data-ttu-id="59835-123">만들 ASR 네트워크 매핑의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59835-123">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="59835-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="59835-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="59835-125">매핑에 대 한 기본 네트워크의 Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="59835-126">-PrimaryFabric</span></span>
<span data-ttu-id="59835-127">매핑을 만들어야 하는 ASR 패브릭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="59835-128">-PrimaryNetwork</span></span>
<span data-ttu-id="59835-129">ASR 네트워크 매핑에 대 한 기본 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59835-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="59835-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="59835-131">네트워크 매핑의 복구 azure 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="59835-132">-RecoveryFabric</span></span>
<span data-ttu-id="59835-133">복구 Azure 지역에 해당 하는 Azure Site Recovery fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59835-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="59835-134">-RecoveryNetwork</span></span>
<span data-ttu-id="59835-135">ASR 네트워크 매핑에 대 한 복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59835-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59835-136">-WhatIf</span></span>
<span data-ttu-id="59835-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59835-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59835-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59835-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59835-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59835-139">CommonParameters</span></span>
<span data-ttu-id="59835-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59835-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59835-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59835-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59835-142">입력</span><span class="sxs-lookup"><span data-stu-id="59835-142">INPUTS</span></span>

### <span data-ttu-id="59835-143">SiteRecovery. r m/. m g 네트워크</span><span class="sxs-lookup"><span data-stu-id="59835-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="59835-144">출력</span><span class="sxs-lookup"><span data-stu-id="59835-144">OUTPUTS</span></span>

### <span data-ttu-id="59835-145">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="59835-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="59835-146">상속자</span><span class="sxs-lookup"><span data-stu-id="59835-146">NOTES</span></span>

## <span data-ttu-id="59835-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59835-147">RELATED LINKS</span></span>

[<span data-ttu-id="59835-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="59835-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="59835-149">제거-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="59835-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)