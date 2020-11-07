---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 6ca4eeba17af918ec73f0fe108b4179ea6513e2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874472"
---
# <span data-ttu-id="9b005-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="9b005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b005-102">SYNOPSIS</span></span>
<span data-ttu-id="9b005-103">Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="9b005-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b005-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b005-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b005-105">DESCRIPTION</span></span>
<span data-ttu-id="9b005-106">**AzWebAppSlot** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9b005-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b005-107">EXAMPLES</span></span>

### <span data-ttu-id="9b005-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b005-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="9b005-109">이 명령은 data center ContosoSite에서 Default-WestUS 이라는 기존 리소스 그룹의 기존 웹 앱 이름 아래에 Slot001 라는 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9b005-110">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9b005-111">변수</span><span class="sxs-lookup"><span data-stu-id="9b005-111">PARAMETERS</span></span>

### <span data-ttu-id="9b005-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b005-112">-AppServicePlan</span></span>
<span data-ttu-id="9b005-113">App Service 계획 이름 또는 앱 서비스 계획 Id입니다. 슬롯 및 앱 서비스 계획이 서로 다른 리소스 그룹에 있는 경우 이름 대신 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="9b005-114">앱 서비스 계획 Id는: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp를 사용 하 여 검색할 수 있습니다. Id는 앱 서비스 계획 Id를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9b005-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="9b005-116">앱 설정이 Hashtable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="9b005-117">-AseName</span></span>
<span data-ttu-id="9b005-118">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b005-119">-AseResourceGroupName</span></span>
<span data-ttu-id="9b005-120">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b005-121">-AsJob</span></span>
<span data-ttu-id="9b005-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9b005-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b005-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9b005-123">-ContainerImageName</span></span>
<span data-ttu-id="9b005-124">컨테이너 이미지 이름 및 선택적 태그 (예: Image: tag)</span><span class="sxs-lookup"><span data-stu-id="9b005-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9b005-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9b005-126">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="9b005-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9b005-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9b005-128">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="9b005-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9b005-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="9b005-130">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b005-131">-DefaultProfile</span></span>
<span data-ttu-id="9b005-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b005-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9b005-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9b005-134">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9b005-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9b005-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9b005-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9b005-136">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="9b005-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9b005-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="9b005-138">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="9b005-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-139">-이름</span><span class="sxs-lookup"><span data-stu-id="9b005-139">-Name</span></span>
<span data-ttu-id="9b005-140">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b005-141">-ResourceGroupName</span></span>
<span data-ttu-id="9b005-142">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-143">-슬롯</span><span class="sxs-lookup"><span data-stu-id="9b005-143">-Slot</span></span>
<span data-ttu-id="9b005-144">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="9b005-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9b005-145">-SourceWebApp</span></span>
<span data-ttu-id="9b005-146">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="9b005-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b005-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b005-147">CommonParameters</span></span>
<span data-ttu-id="9b005-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b005-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b005-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b005-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b005-150">입력</span><span class="sxs-lookup"><span data-stu-id="9b005-150">INPUTS</span></span>

### <span data-ttu-id="9b005-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b005-151">System.String</span></span>

### <span data-ttu-id="9b005-152">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="9b005-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9b005-153">출력</span><span class="sxs-lookup"><span data-stu-id="9b005-153">OUTPUTS</span></span>

### <span data-ttu-id="9b005-154">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="9b005-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9b005-155">상속자</span><span class="sxs-lookup"><span data-stu-id="9b005-155">NOTES</span></span>

## <span data-ttu-id="9b005-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b005-156">RELATED LINKS</span></span>

[<span data-ttu-id="9b005-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="9b005-158">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9b005-159">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9b005-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9b005-161">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="9b005-162">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b005-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9b005-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b005-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="9b005-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9b005-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)