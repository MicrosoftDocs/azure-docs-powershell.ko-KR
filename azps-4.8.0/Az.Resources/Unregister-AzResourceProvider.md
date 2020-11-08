---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204373"
---
# <span data-ttu-id="0e8cc-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e8cc-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="0e8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8cc-103">리소스 공급자의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="0e8cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e8cc-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8cc-106">AzResourceProvider cmdlet은 Azure 리소스 공급자의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="0e8cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e8cc-107">EXAMPLES</span></span>

### <span data-ttu-id="0e8cc-108">예제 1: ProviderNamespace를 사용 하 여 리소스 공급자 등록 취소</span><span class="sxs-lookup"><span data-stu-id="0e8cc-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="0e8cc-109">이 명령은 리소스 공급자 "Microsoft. 지원"의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="0e8cc-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e8cc-110">PARAMETERS</span></span>

### <span data-ttu-id="0e8cc-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e8cc-111">-ApiVersion</span></span>
<span data-ttu-id="0e8cc-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0e8cc-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0e8cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8cc-114">-DefaultProfile</span></span>
<span data-ttu-id="0e8cc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e8cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8cc-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="0e8cc-116">-Pre</span></span>
<span data-ttu-id="0e8cc-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0e8cc-118">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0e8cc-118">-ProviderNamespace</span></span>
<span data-ttu-id="0e8cc-119">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="0e8cc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="0e8cc-120">-Confirm</span></span>
<span data-ttu-id="0e8cc-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8cc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8cc-122">-WhatIf</span></span>
<span data-ttu-id="0e8cc-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8cc-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8cc-125">CommonParameters</span></span>
<span data-ttu-id="0e8cc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8cc-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8cc-128">입력</span><span class="sxs-lookup"><span data-stu-id="0e8cc-128">INPUTS</span></span>

### <span data-ttu-id="0e8cc-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e8cc-129">System.String</span></span>

## <span data-ttu-id="0e8cc-130">출력</span><span class="sxs-lookup"><span data-stu-id="0e8cc-130">OUTPUTS</span></span>

### <span data-ttu-id="0e8cc-131">SdkModels. PSResourceProvider에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="0e8cc-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="0e8cc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0e8cc-132">NOTES</span></span>

## <span data-ttu-id="0e8cc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8cc-133">RELATED LINKS</span></span>

[<span data-ttu-id="0e8cc-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e8cc-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="0e8cc-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e8cc-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

