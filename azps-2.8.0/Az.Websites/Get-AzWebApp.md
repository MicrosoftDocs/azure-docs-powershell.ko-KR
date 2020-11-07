---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869529"
---
# <span data-ttu-id="31e38-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-101">Get-AzWebApp</span></span>

## <span data-ttu-id="31e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e38-102">SYNOPSIS</span></span>
<span data-ttu-id="31e38-103">지정 된 리소스 그룹의 Azure 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31e38-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="31e38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31e38-104">SYNTAX</span></span>

### <span data-ttu-id="31e38-105">S1</span><span class="sxs-lookup"><span data-stu-id="31e38-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31e38-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="31e38-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31e38-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="31e38-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e38-108">설명은</span><span class="sxs-lookup"><span data-stu-id="31e38-108">DESCRIPTION</span></span>
<span data-ttu-id="31e38-109">**AzWebApp** Cmdlet은 Azure 웹 앱에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31e38-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="31e38-110">예제의</span><span class="sxs-lookup"><span data-stu-id="31e38-110">EXAMPLES</span></span>

### <span data-ttu-id="31e38-111">예제 1: 리소스 그룹에서 웹 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="31e38-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="31e38-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31e38-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="31e38-113">변수</span><span class="sxs-lookup"><span data-stu-id="31e38-113">PARAMETERS</span></span>

### <span data-ttu-id="31e38-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="31e38-114">-AppServicePlan</span></span>
<span data-ttu-id="31e38-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="31e38-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e38-116">-DefaultProfile</span></span>
<span data-ttu-id="31e38-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31e38-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e38-118">-위치</span><span class="sxs-lookup"><span data-stu-id="31e38-118">-Location</span></span>
<span data-ttu-id="31e38-119">Location</span><span class="sxs-lookup"><span data-stu-id="31e38-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e38-120">-이름</span><span class="sxs-lookup"><span data-stu-id="31e38-120">-Name</span></span>
<span data-ttu-id="31e38-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="31e38-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e38-122">-ResourceGroupName</span></span>
<span data-ttu-id="31e38-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="31e38-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e38-124">CommonParameters</span></span>
<span data-ttu-id="31e38-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e38-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e38-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e38-127">입력</span><span class="sxs-lookup"><span data-stu-id="31e38-127">INPUTS</span></span>

### <span data-ttu-id="31e38-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31e38-128">System.String</span></span>

## <span data-ttu-id="31e38-129">출력</span><span class="sxs-lookup"><span data-stu-id="31e38-129">OUTPUTS</span></span>

### <span data-ttu-id="31e38-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="31e38-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="31e38-131">상속자</span><span class="sxs-lookup"><span data-stu-id="31e38-131">NOTES</span></span>

## <span data-ttu-id="31e38-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31e38-132">RELATED LINKS</span></span>

[<span data-ttu-id="31e38-133">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="31e38-134">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="31e38-135">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="31e38-136">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="31e38-137">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31e38-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

