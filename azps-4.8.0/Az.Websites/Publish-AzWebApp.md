---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056033"
---
# <span data-ttu-id="08a3f-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="08a3f-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="08a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="08a3f-103">Zipdeploy를 사용 하 여 ZIP, JAR 또는 WAR 파일에서 Azure 웹 앱을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="08a3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08a3f-104">SYNTAX</span></span>

### <span data-ttu-id="08a3f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="08a3f-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08a3f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="08a3f-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="08a3f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="08a3f-107">DESCRIPTION</span></span>
<span data-ttu-id="08a3f-108">**AzWebApp** cmdlet은 콘텐츠를 기존 Azure Web App에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="08a3f-109">.NET, Python 또는 Node와 같은 스택을 사용 하거나, Java를 사용 하는 경우 WAR 또는 JAR 파일의 경우 콘텐츠는 ZIP 파일에 패키지 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="08a3f-110">배포 중에 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 실행할 준비가 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="08a3f-111">이 cmdlet은 Kudu zipdeploy 및 워 하는 배포 기능을 사용 하 여 콘텐츠를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="08a3f-112">Zipdeploy 및 Kudu에서 작업을 배포 하는 방법과 배포를 위해 웹 앱을 올바르게 패키지 하는 방법에 대 한 자세한 내용은 wiki를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08a3f-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="08a3f-113"> https://aka.ms/kuduzipdeployhttps://aka.ms/kuduwardeployzipdeploy 및 워 배포에 대 한 유용한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="08a3f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="08a3f-114">EXAMPLES</span></span>

### <span data-ttu-id="08a3f-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="08a3f-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="08a3f-116">리소스 그룹 Default-WestUS에 속하는 MyApp 라는 웹 앱에 app.zip의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="08a3f-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="08a3f-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="08a3f-118">리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱의 스테이징 슬롯에 javaproject의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="08a3f-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="08a3f-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="08a3f-120">app.zip의 콘텐츠를 리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="08a3f-121">Cmdlet은 백그라운드 작업에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="08a3f-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="08a3f-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="08a3f-123">예제 5</span><span class="sxs-lookup"><span data-stu-id="08a3f-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="08a3f-124">리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 .jar java_app의 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="08a3f-125">변수</span><span class="sxs-lookup"><span data-stu-id="08a3f-125">PARAMETERS</span></span>

### <span data-ttu-id="08a3f-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="08a3f-126">-ArchivePath</span></span>
<span data-ttu-id="08a3f-127">보관 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-127">The path of the archive file.</span></span> <span data-ttu-id="08a3f-128">ZIP, 전쟁, JAR를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a3f-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08a3f-129">-AsJob</span></span>
<span data-ttu-id="08a3f-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="08a3f-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08a3f-131">-Force</span><span class="sxs-lookup"><span data-stu-id="08a3f-131">-Force</span></span>
<span data-ttu-id="08a3f-132">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="08a3f-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="08a3f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a3f-133">-DefaultProfile</span></span>
<span data-ttu-id="08a3f-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08a3f-135">-이름</span><span class="sxs-lookup"><span data-stu-id="08a3f-135">-Name</span></span>
<span data-ttu-id="08a3f-136">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-136">The name of the web app.</span></span>

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

### <span data-ttu-id="08a3f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a3f-137">-ResourceGroupName</span></span>
<span data-ttu-id="08a3f-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="08a3f-139">-슬롯</span><span class="sxs-lookup"><span data-stu-id="08a3f-139">-Slot</span></span>
<span data-ttu-id="08a3f-140">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="08a3f-141">-Web app</span><span class="sxs-lookup"><span data-stu-id="08a3f-141">-WebApp</span></span>
<span data-ttu-id="08a3f-142">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="08a3f-142">The web app object</span></span>

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

### <span data-ttu-id="08a3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a3f-143">CommonParameters</span></span>
<span data-ttu-id="08a3f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08a3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a3f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08a3f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a3f-146">입력</span><span class="sxs-lookup"><span data-stu-id="08a3f-146">INPUTS</span></span>

### <span data-ttu-id="08a3f-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08a3f-147">System.String</span></span>

### <span data-ttu-id="08a3f-148">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="08a3f-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08a3f-149">출력</span><span class="sxs-lookup"><span data-stu-id="08a3f-149">OUTPUTS</span></span>

### <span data-ttu-id="08a3f-150">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="08a3f-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08a3f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="08a3f-151">NOTES</span></span>

## <span data-ttu-id="08a3f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08a3f-152">RELATED LINKS</span></span>