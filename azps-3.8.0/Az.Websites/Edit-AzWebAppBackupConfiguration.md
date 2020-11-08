---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041677"
---
# <span data-ttu-id="84c4d-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="84c4d-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="84c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84c4d-102">SYNOPSIS</span></span>

## <span data-ttu-id="84c4d-103">구문과</span><span class="sxs-lookup"><span data-stu-id="84c4d-103">SYNTAX</span></span>

### <span data-ttu-id="84c4d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="84c4d-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="84c4d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="84c4d-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="84c4d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="84c4d-106">DESCRIPTION</span></span>
<span data-ttu-id="84c4d-107">**편집-AzWebAppBackupConfiguration** Cmdlet은 Azure Web App에 대 한 현재 구성 백업을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="84c4d-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="84c4d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="84c4d-108">EXAMPLES</span></span>

## <span data-ttu-id="84c4d-109">변수</span><span class="sxs-lookup"><span data-stu-id="84c4d-109">PARAMETERS</span></span>

### <span data-ttu-id="84c4d-110">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="84c4d-110">-Databases</span></span>
<span data-ttu-id="84c4d-111">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="84c4d-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c4d-112">-DefaultProfile</span></span>
<span data-ttu-id="84c4d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84c4d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c4d-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="84c4d-114">-FrequencyInterval</span></span>
<span data-ttu-id="84c4d-115">빈도 간격</span><span class="sxs-lookup"><span data-stu-id="84c4d-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="84c4d-116">-FrequencyUnit</span></span>
<span data-ttu-id="84c4d-117">주파수 단위</span><span class="sxs-lookup"><span data-stu-id="84c4d-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="84c4d-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="84c4d-119">하나 이상의 백업 옵션 유지</span><span class="sxs-lookup"><span data-stu-id="84c4d-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="84c4d-120">-Name</span></span>
<span data-ttu-id="84c4d-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="84c4d-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="84c4d-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="84c4d-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="84c4d-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="84c4d-125">보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="84c4d-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-126">-슬롯</span><span class="sxs-lookup"><span data-stu-id="84c4d-126">-Slot</span></span>
<span data-ttu-id="84c4d-127">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="84c4d-127">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="84c4d-128">-StartTime</span></span>
<span data-ttu-id="84c4d-129">UTC의 StartTime</span><span class="sxs-lookup"><span data-stu-id="84c4d-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="84c4d-130">-StorageAccountUrl</span></span>
<span data-ttu-id="84c4d-131">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="84c4d-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-132">-Web app</span><span class="sxs-lookup"><span data-stu-id="84c4d-132">-WebApp</span></span>
<span data-ttu-id="84c4d-133">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="84c4d-133">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c4d-134">CommonParameters</span></span>
<span data-ttu-id="84c4d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84c4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c4d-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c4d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c4d-137">입력</span><span class="sxs-lookup"><span data-stu-id="84c4d-137">INPUTS</span></span>

### <span data-ttu-id="84c4d-138">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="84c4d-138">System.Int32</span></span>

### <span data-ttu-id="84c4d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84c4d-139">System.String</span></span>

### <span data-ttu-id="84c4d-140">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="84c4d-140">System.DateTime</span></span>

### <span data-ttu-id="84c4d-141">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="84c4d-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="84c4d-142">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="84c4d-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="84c4d-143">DatabaseBackupSetting [] (으)로</span><span class="sxs-lookup"><span data-stu-id="84c4d-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="84c4d-144">출력</span><span class="sxs-lookup"><span data-stu-id="84c4d-144">OUTPUTS</span></span>

### <span data-ttu-id="84c4d-145">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="84c4d-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="84c4d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="84c4d-146">NOTES</span></span>

## <span data-ttu-id="84c4d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84c4d-147">RELATED LINKS</span></span>

[<span data-ttu-id="84c4d-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="84c4d-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)

