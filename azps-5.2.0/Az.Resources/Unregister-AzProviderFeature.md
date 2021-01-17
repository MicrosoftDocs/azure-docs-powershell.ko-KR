---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345074"
---
# <span data-ttu-id="4ec1a-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4ec1a-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="4ec1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec1a-103">계정에서 Azure 공급자 기능을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="4ec1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ec1a-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec1a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4ec1a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec1a-106">**Unregister-AzProviderFeature** cmdlet은 계정에서 Azure 공급자 기능을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="4ec1a-107">예제</span><span class="sxs-lookup"><span data-stu-id="4ec1a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec1a-108">예제 1: 기능 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="4ec1a-109">그러면 계정에서 Microsoft.Network에 대한 AllowApplicationSecurityGroups 기능이 등록되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="4ec1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ec1a-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec1a-111">-DefaultProfile</span></span>
<span data-ttu-id="4ec1a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec1a-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="4ec1a-113">-FeatureName</span></span>
<span data-ttu-id="4ec1a-114">기능 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec1a-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4ec1a-115">-ProviderNamespace</span></span>
<span data-ttu-id="4ec1a-116">리소스 공급자 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec1a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ec1a-117">-Confirm</span></span>
<span data-ttu-id="4ec1a-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec1a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec1a-119">-WhatIf</span></span>
<span data-ttu-id="4ec1a-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4ec1a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec1a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec1a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec1a-122">CommonParameters</span></span>
<span data-ttu-id="4ec1a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec1a-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ec1a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec1a-125">입력</span><span class="sxs-lookup"><span data-stu-id="4ec1a-125">INPUTS</span></span>

### <span data-ttu-id="4ec1a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec1a-126">System.String</span></span>

## <span data-ttu-id="4ec1a-127">출력</span><span class="sxs-lookup"><span data-stu-id="4ec1a-127">OUTPUTS</span></span>

### <span data-ttu-id="4ec1a-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4ec1a-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="4ec1a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ec1a-129">NOTES</span></span>

## <span data-ttu-id="4ec1a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ec1a-130">RELATED LINKS</span></span>