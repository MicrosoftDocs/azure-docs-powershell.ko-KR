---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868621"
---
# <span data-ttu-id="4cfde-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4cfde-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4cfde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfde-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfde-103">Data Lake Analytics 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4cfde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cfde-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cfde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cfde-105">DESCRIPTION</span></span>
<span data-ttu-id="4cfde-106">**AzDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4cfde-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4cfde-107">EXAMPLES</span></span>

### <span data-ttu-id="4cfde-108">예제 1: 계정 제거</span><span class="sxs-lookup"><span data-stu-id="4cfde-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="4cfde-109">이 명령은 지정 된 Data Lake Analytics 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="4cfde-110">변수</span><span class="sxs-lookup"><span data-stu-id="4cfde-110">PARAMETERS</span></span>

### <span data-ttu-id="4cfde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfde-111">-DefaultProfile</span></span>
<span data-ttu-id="4cfde-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4cfde-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cfde-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4cfde-113">-Force</span></span>
<span data-ttu-id="4cfde-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cfde-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4cfde-115">-Name</span></span>
<span data-ttu-id="4cfde-116">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4cfde-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cfde-117">-PassThru</span></span>
<span data-ttu-id="4cfde-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4cfde-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4cfde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfde-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cfde-121">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4cfde-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4cfde-122">-Confirm</span></span>
<span data-ttu-id="4cfde-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cfde-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cfde-124">-WhatIf</span></span>
<span data-ttu-id="4cfde-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cfde-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cfde-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfde-127">CommonParameters</span></span>
<span data-ttu-id="4cfde-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cfde-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfde-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cfde-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfde-130">입력</span><span class="sxs-lookup"><span data-stu-id="4cfde-130">INPUTS</span></span>

### <span data-ttu-id="4cfde-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4cfde-131">System.String</span></span>

## <span data-ttu-id="4cfde-132">출력</span><span class="sxs-lookup"><span data-stu-id="4cfde-132">OUTPUTS</span></span>

### <span data-ttu-id="4cfde-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4cfde-133">System.Boolean</span></span>

## <span data-ttu-id="4cfde-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4cfde-134">NOTES</span></span>

## <span data-ttu-id="4cfde-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cfde-135">RELATED LINKS</span></span>

[<span data-ttu-id="4cfde-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4cfde-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4cfde-137">새로운 AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4cfde-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4cfde-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4cfde-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4cfde-139">테스트-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4cfde-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

