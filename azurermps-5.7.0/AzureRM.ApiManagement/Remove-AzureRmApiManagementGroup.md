---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535363"
---
# <span data-ttu-id="d7761-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7761-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d7761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7761-102">SYNOPSIS</span></span>
<span data-ttu-id="d7761-103">기존 API 관리 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7761-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7761-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7761-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7761-105">DESCRIPTION</span></span>
<span data-ttu-id="d7761-106">**AzureRmApiManagementGroup** cmdlet은 기존 API 관리 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="d7761-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7761-107">EXAMPLES</span></span>

### <span data-ttu-id="d7761-108">예제 1: 기존 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="d7761-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="d7761-109">이 명령은 Group0001 이라는 기존 관리 그룹을 제거 하 고 사용자에 게 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="d7761-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7761-110">PARAMETERS</span></span>

### <span data-ttu-id="d7761-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d7761-111">-Context</span></span>
<span data-ttu-id="d7761-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7761-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7761-113">-DefaultProfile</span></span>
<span data-ttu-id="d7761-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7761-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d7761-115">-GroupId</span></span>
<span data-ttu-id="d7761-116">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="d7761-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7761-117">-PassThru</span></span>
<span data-ttu-id="d7761-118">이 cmdlet이 성공할 경우 $True 값을 반환 하거나, $False 값이 없는 경우, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7761-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d7761-119">-Confirm</span></span>
<span data-ttu-id="d7761-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7761-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7761-121">-WhatIf</span></span>
<span data-ttu-id="d7761-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7761-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7761-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7761-124">CommonParameters</span></span>
<span data-ttu-id="d7761-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7761-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7761-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7761-127">입력</span><span class="sxs-lookup"><span data-stu-id="d7761-127">INPUTS</span></span>

### <span data-ttu-id="d7761-128">않아야</span><span class="sxs-lookup"><span data-stu-id="d7761-128">None</span></span>
<span data-ttu-id="d7761-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7761-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7761-130">출력</span><span class="sxs-lookup"><span data-stu-id="d7761-130">OUTPUTS</span></span>

### <span data-ttu-id="d7761-131">나타내는</span><span class="sxs-lookup"><span data-stu-id="d7761-131">Boolean</span></span>

## <span data-ttu-id="d7761-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d7761-132">NOTES</span></span>

## <span data-ttu-id="d7761-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7761-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7761-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7761-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d7761-135">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7761-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d7761-136">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7761-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)

