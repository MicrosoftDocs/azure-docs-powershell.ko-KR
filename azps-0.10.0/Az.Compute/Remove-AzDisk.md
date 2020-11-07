---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876972"
---
# <span data-ttu-id="c4172-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="c4172-101">Remove-AzDisk</span></span>

## <span data-ttu-id="c4172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4172-102">SYNOPSIS</span></span>
<span data-ttu-id="c4172-103">디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-103">Removes a disk.</span></span>

## <span data-ttu-id="c4172-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4172-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4172-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4172-105">DESCRIPTION</span></span>
<span data-ttu-id="c4172-106">**AzDisk** cmdlet이 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="c4172-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4172-107">EXAMPLES</span></span>

### <span data-ttu-id="c4172-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4172-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="c4172-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c4172-110">변수</span><span class="sxs-lookup"><span data-stu-id="c4172-110">PARAMETERS</span></span>

### <span data-ttu-id="c4172-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4172-111">-AsJob</span></span>
<span data-ttu-id="c4172-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4172-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4172-113">-DefaultProfile</span></span>
<span data-ttu-id="c4172-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4172-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c4172-115">-DiskName</span></span>
<span data-ttu-id="c4172-116">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4172-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c4172-117">-Force</span></span>
<span data-ttu-id="c4172-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4172-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4172-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4172-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4172-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c4172-121">-Confirm</span></span>
<span data-ttu-id="c4172-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4172-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4172-123">-WhatIf</span></span>
<span data-ttu-id="c4172-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4172-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4172-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4172-126">CommonParameters</span></span>
<span data-ttu-id="c4172-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4172-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4172-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4172-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4172-129">입력</span><span class="sxs-lookup"><span data-stu-id="c4172-129">INPUTS</span></span>

### <span data-ttu-id="c4172-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4172-130">System.String</span></span>

## <span data-ttu-id="c4172-131">출력</span><span class="sxs-lookup"><span data-stu-id="c4172-131">OUTPUTS</span></span>

### <span data-ttu-id="c4172-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c4172-132">System.Object</span></span>

## <span data-ttu-id="c4172-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c4172-133">NOTES</span></span>

## <span data-ttu-id="c4172-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4172-134">RELATED LINKS</span></span>
