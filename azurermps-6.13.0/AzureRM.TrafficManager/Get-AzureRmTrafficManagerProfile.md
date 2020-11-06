---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525939"
---
# <span data-ttu-id="7d3f6-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="7d3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3f6-103">Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d3f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d3f6-104">SYNTAX</span></span>

### <span data-ttu-id="7d3f6-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3f6-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d3f6-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3f6-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d3f6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d3f6-107">DESCRIPTION</span></span>
<span data-ttu-id="7d3f6-108">**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 가져오고 해당 프로필을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="7d3f6-109">프로필 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="7d3f6-110">이 개체를 로컬로 수정한 다음 Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="7d3f6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7d3f6-111">EXAMPLES</span></span>

### <span data-ttu-id="7d3f6-112">예제 1: 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="7d3f6-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7d3f6-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="7d3f6-114">변수</span><span class="sxs-lookup"><span data-stu-id="7d3f6-114">PARAMETERS</span></span>

### <span data-ttu-id="7d3f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-115">-DefaultProfile</span></span>
<span data-ttu-id="7d3f6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d3f6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7d3f6-117">-Name</span></span>
<span data-ttu-id="7d3f6-118">이 cmdlet이 가져오는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d3f6-120">이 cmdlet이 가져오는 Traffic Manager 프로필을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3f6-121">CommonParameters</span></span>
<span data-ttu-id="7d3f6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3f6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3f6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3f6-124">입력</span><span class="sxs-lookup"><span data-stu-id="7d3f6-124">INPUTS</span></span>

### <span data-ttu-id="7d3f6-125">않아야</span><span class="sxs-lookup"><span data-stu-id="7d3f6-125">None</span></span>
<span data-ttu-id="7d3f6-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d3f6-127">출력</span><span class="sxs-lookup"><span data-stu-id="7d3f6-127">OUTPUTS</span></span>

### <span data-ttu-id="7d3f6-128">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="7d3f6-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7d3f6-129">이 cmdlet은 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7d3f6-130">이 개체를 수정한 다음 **Set-AzureRmTrafficManagerProfile** 를 사용 하 여 트래픽 관리자에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="7d3f6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7d3f6-131">NOTES</span></span>

## <span data-ttu-id="7d3f6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d3f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d3f6-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d3f6-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d3f6-135">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d3f6-136">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d3f6-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

