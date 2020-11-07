---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 46a18d981bae7a8528a866d4f21cf5b07b64732f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871846"
---
# <span data-ttu-id="7fd7c-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7fd7c-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="7fd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd7c-103">Azure 공급자 기능에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="7fd7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fd7c-104">SYNTAX</span></span>

### <span data-ttu-id="7fd7c-105">ListAvailableParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7fd7c-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd7c-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="7fd7c-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7fd7c-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd7c-108">**AzProviderFeature** cmdlet은 기능 이름, 공급자 이름 및 Azure 공급자 기능에 대 한 등록 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="7fd7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7fd7c-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd7c-110">예제 1: 사용할 수 있는 모든 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="7fd7c-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="7fd7c-111">이 명령은 사용할 수 있는 모든 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-111">This command gets all available features.</span></span>

### <span data-ttu-id="7fd7c-112">예제 2: 특정 기능에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7fd7c-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="7fd7c-113">이 명령은 지정 된 공급자에 대 한 AllowPreReleaseRegions 이라는 기능에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="7fd7c-114">변수</span><span class="sxs-lookup"><span data-stu-id="7fd7c-114">PARAMETERS</span></span>

### <span data-ttu-id="7fd7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd7c-115">-DefaultProfile</span></span>
<span data-ttu-id="7fd7c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7fd7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fd7c-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7fd7c-117">-FeatureName</span></span>
<span data-ttu-id="7fd7c-118">가져올 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd7c-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7fd7c-119">-ListAvailable</span></span>
<span data-ttu-id="7fd7c-120">이 cmdlet에 모든 기능이 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd7c-121">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7fd7c-121">-ProviderNamespace</span></span>
<span data-ttu-id="7fd7c-122">이 cmdlet이 공급자 기능을 가져오는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd7c-123">CommonParameters</span></span>
<span data-ttu-id="7fd7c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd7c-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd7c-126">입력</span><span class="sxs-lookup"><span data-stu-id="7fd7c-126">INPUTS</span></span>

### <span data-ttu-id="7fd7c-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7fd7c-127">System.String</span></span>

## <span data-ttu-id="7fd7c-128">출력</span><span class="sxs-lookup"><span data-stu-id="7fd7c-128">OUTPUTS</span></span>

### <span data-ttu-id="7fd7c-129">SdkModels PSProviderFeature. m m m 기능</span><span class="sxs-lookup"><span data-stu-id="7fd7c-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="7fd7c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="7fd7c-130">NOTES</span></span>

## <span data-ttu-id="7fd7c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fd7c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7fd7c-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7fd7c-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)

