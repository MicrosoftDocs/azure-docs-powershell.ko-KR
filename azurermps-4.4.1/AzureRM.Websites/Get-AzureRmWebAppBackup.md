---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532195"
---
# <span data-ttu-id="fa5c0-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fa5c0-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="fa5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa5c0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa5c0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="fa5c0-103">SYNTAX</span></span>

### <span data-ttu-id="fa5c0-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fa5c0-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5c0-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fa5c0-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa5c0-106">설명은</span><span class="sxs-lookup"><span data-stu-id="fa5c0-106">DESCRIPTION</span></span>
<span data-ttu-id="fa5c0-107">**AzureRmWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="fa5c0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fa5c0-108">EXAMPLES</span></span>

### <span data-ttu-id="fa5c0-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="fa5c0-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="fa5c0-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="fa5c0-111">변수</span><span class="sxs-lookup"><span data-stu-id="fa5c0-111">PARAMETERS</span></span>

### <span data-ttu-id="fa5c0-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="fa5c0-112">-BackupId</span></span>
<span data-ttu-id="fa5c0-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="fa5c0-113">Backup Id</span></span>

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

### <span data-ttu-id="fa5c0-114">-이름</span><span class="sxs-lookup"><span data-stu-id="fa5c0-114">-Name</span></span>
<span data-ttu-id="fa5c0-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fa5c0-115">Webapp Name</span></span>

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

### <span data-ttu-id="fa5c0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5c0-116">-ResourceGroupName</span></span>
<span data-ttu-id="fa5c0-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fa5c0-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fa5c0-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fa5c0-118">-Slot</span></span>
<span data-ttu-id="fa5c0-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fa5c0-119">Slot Name</span></span>

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

### <span data-ttu-id="fa5c0-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="fa5c0-120">-WebApp</span></span>
<span data-ttu-id="fa5c0-121">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="fa5c0-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5c0-122">-DefaultProfile</span></span>
<span data-ttu-id="fa5c0-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa5c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5c0-124">CommonParameters</span></span>
<span data-ttu-id="fa5c0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5c0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5c0-127">입력</span><span class="sxs-lookup"><span data-stu-id="fa5c0-127">INPUTS</span></span>

### <span data-ttu-id="fa5c0-128">Site</span><span class="sxs-lookup"><span data-stu-id="fa5c0-128">Site</span></span>
<span data-ttu-id="fa5c0-129">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fa5c0-130">출력</span><span class="sxs-lookup"><span data-stu-id="fa5c0-130">OUTPUTS</span></span>

### <span data-ttu-id="fa5c0-131">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="fa5c0-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="fa5c0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fa5c0-132">NOTES</span></span>

## <span data-ttu-id="fa5c0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa5c0-133">RELATED LINKS</span></span>
