---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527624"
---
# <span data-ttu-id="07921-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="07921-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="07921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07921-102">SYNOPSIS</span></span>
<span data-ttu-id="07921-103">Data Lake Analytics 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07921-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07921-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07921-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07921-105">DESCRIPTION</span></span>
<span data-ttu-id="07921-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="07921-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07921-107">EXAMPLES</span></span>

### <span data-ttu-id="07921-108">예제 1: 계정 제거</span><span class="sxs-lookup"><span data-stu-id="07921-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="07921-109">이 명령은 지정 된 Data Lake Analytics 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="07921-110">변수</span><span class="sxs-lookup"><span data-stu-id="07921-110">PARAMETERS</span></span>

### <span data-ttu-id="07921-111">-Force</span><span class="sxs-lookup"><span data-stu-id="07921-111">-Force</span></span>
<span data-ttu-id="07921-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07921-113">-이름</span><span class="sxs-lookup"><span data-stu-id="07921-113">-Name</span></span>
<span data-ttu-id="07921-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07921-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07921-115">-PassThru</span></span>
<span data-ttu-id="07921-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07921-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07921-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07921-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07921-118">-ResourceGroupName</span></span>
<span data-ttu-id="07921-119">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07921-120">-확인</span><span class="sxs-lookup"><span data-stu-id="07921-120">-Confirm</span></span>
<span data-ttu-id="07921-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07921-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07921-122">-WhatIf</span></span>
<span data-ttu-id="07921-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07921-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07921-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07921-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07921-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07921-125">-DefaultProfile</span></span>
<span data-ttu-id="07921-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07921-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07921-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07921-127">CommonParameters</span></span>
<span data-ttu-id="07921-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07921-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07921-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07921-130">입력</span><span class="sxs-lookup"><span data-stu-id="07921-130">INPUTS</span></span>

## <span data-ttu-id="07921-131">출력</span><span class="sxs-lookup"><span data-stu-id="07921-131">OUTPUTS</span></span>

### <span data-ttu-id="07921-132">부울</span><span class="sxs-lookup"><span data-stu-id="07921-132">bool</span></span>
<span data-ttu-id="07921-133">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07921-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="07921-134">상속자</span><span class="sxs-lookup"><span data-stu-id="07921-134">NOTES</span></span>

## <span data-ttu-id="07921-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07921-135">RELATED LINKS</span></span>

[<span data-ttu-id="07921-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="07921-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="07921-137">새로운 AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="07921-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="07921-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="07921-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="07921-139">테스트-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="07921-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)

