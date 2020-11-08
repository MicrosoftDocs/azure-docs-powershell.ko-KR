---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: 04184483d2bda7495014d3efd8ecf35b4d3b6864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034186"
---
# <span data-ttu-id="c9a35-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c9a35-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="c9a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a35-102">SYNOPSIS</span></span>

## <span data-ttu-id="c9a35-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c9a35-103">SYNTAX</span></span>

### <span data-ttu-id="c9a35-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c9a35-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a35-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c9a35-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9a35-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c9a35-106">DESCRIPTION</span></span>
<span data-ttu-id="c9a35-107">**AzWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a35-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="c9a35-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c9a35-108">EXAMPLES</span></span>

### <span data-ttu-id="c9a35-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="c9a35-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="c9a35-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 사용 하 여 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a35-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c9a35-111">변수</span><span class="sxs-lookup"><span data-stu-id="c9a35-111">PARAMETERS</span></span>

### <span data-ttu-id="c9a35-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c9a35-112">-BackupId</span></span>
<span data-ttu-id="c9a35-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="c9a35-113">Backup Id</span></span>

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

### <span data-ttu-id="c9a35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a35-114">-DefaultProfile</span></span>
<span data-ttu-id="c9a35-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a35-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9a35-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c9a35-116">-Name</span></span>
<span data-ttu-id="c9a35-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="c9a35-117">WebApp Name</span></span>

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

### <span data-ttu-id="c9a35-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a35-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9a35-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c9a35-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c9a35-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c9a35-120">-Slot</span></span>
<span data-ttu-id="c9a35-121">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="c9a35-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c9a35-122">-Web app</span><span class="sxs-lookup"><span data-stu-id="c9a35-122">-WebApp</span></span>
<span data-ttu-id="c9a35-123">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="c9a35-123">WebApp Object</span></span>

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

### <span data-ttu-id="c9a35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a35-124">CommonParameters</span></span>
<span data-ttu-id="c9a35-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a35-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a35-127">입력</span><span class="sxs-lookup"><span data-stu-id="c9a35-127">INPUTS</span></span>

### <span data-ttu-id="c9a35-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9a35-128">System.String</span></span>

### <span data-ttu-id="c9a35-129">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c9a35-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9a35-130">출력</span><span class="sxs-lookup"><span data-stu-id="c9a35-130">OUTPUTS</span></span>

### <span data-ttu-id="c9a35-131">Microsoft. Azure. 관리자.</span><span class="sxs-lookup"><span data-stu-id="c9a35-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="c9a35-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c9a35-132">NOTES</span></span>

## <span data-ttu-id="c9a35-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a35-133">RELATED LINKS</span></span>