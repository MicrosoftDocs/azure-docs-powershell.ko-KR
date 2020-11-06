---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 691378cac3ac721084315a1708bf8d4d0a24dc92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528413"
---
# <span data-ttu-id="71e4a-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="71e4a-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="71e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="71e4a-103">리소스 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71e4a-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="71e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="71e4a-106">**AzureRmResourceProvider** Cmdlet은 Azure 리소스 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="71e4a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="71e4a-108">예제 1: 공급자 등록</span><span class="sxs-lookup"><span data-stu-id="71e4a-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="71e4a-109">계정에 대 한 Microsoft 네트워크 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="71e4a-110">변수</span><span class="sxs-lookup"><span data-stu-id="71e4a-110">PARAMETERS</span></span>

### <span data-ttu-id="71e4a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71e4a-111">-ApiVersion</span></span>
<span data-ttu-id="71e4a-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="71e4a-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="71e4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e4a-114">-DefaultProfile</span></span>
<span data-ttu-id="71e4a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71e4a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e4a-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="71e4a-116">-Pre</span></span>
<span data-ttu-id="71e4a-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71e4a-118">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="71e4a-118">-ProviderNamespace</span></span>
<span data-ttu-id="71e4a-119">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-119">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e4a-120">-확인</span><span class="sxs-lookup"><span data-stu-id="71e4a-120">-Confirm</span></span>
<span data-ttu-id="71e4a-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e4a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e4a-122">-WhatIf</span></span>
<span data-ttu-id="71e4a-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e4a-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e4a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e4a-125">CommonParameters</span></span>
<span data-ttu-id="71e4a-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e4a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e4a-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e4a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e4a-128">입력</span><span class="sxs-lookup"><span data-stu-id="71e4a-128">INPUTS</span></span>

## <span data-ttu-id="71e4a-129">출력</span><span class="sxs-lookup"><span data-stu-id="71e4a-129">OUTPUTS</span></span>

## <span data-ttu-id="71e4a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="71e4a-130">NOTES</span></span>

## <span data-ttu-id="71e4a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71e4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="71e4a-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="71e4a-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="71e4a-133">등록 취소-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="71e4a-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

