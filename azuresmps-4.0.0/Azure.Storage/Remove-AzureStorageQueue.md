---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523915"
---
# <span data-ttu-id="85566-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85566-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="85566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85566-102">SYNOPSIS</span></span>
<span data-ttu-id="85566-103">저장소 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-103">Removes a storage queue.</span></span>

## <span data-ttu-id="85566-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85566-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85566-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85566-105">DESCRIPTION</span></span>
<span data-ttu-id="85566-106">**AzureStorageQueue** cmdlet은 저장소 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="85566-107">예제의</span><span class="sxs-lookup"><span data-stu-id="85566-107">EXAMPLES</span></span>

### <span data-ttu-id="85566-108">예제 1: 이름으로 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="85566-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="85566-109">이 명령은 ContosoQueue01 이라는 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="85566-110">예제 2: 여러 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="85566-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="85566-111">이 명령은 Contoso로 시작 하는 이름의 모든 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="85566-112">변수</span><span class="sxs-lookup"><span data-stu-id="85566-112">PARAMETERS</span></span>

### <span data-ttu-id="85566-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="85566-113">-Context</span></span>
<span data-ttu-id="85566-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="85566-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85566-116">-Force</span><span class="sxs-lookup"><span data-stu-id="85566-116">-Force</span></span>
<span data-ttu-id="85566-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85566-118">-이름</span><span class="sxs-lookup"><span data-stu-id="85566-118">-Name</span></span>
<span data-ttu-id="85566-119">제거할 대기열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85566-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85566-120">-PassThru</span></span>
<span data-ttu-id="85566-121">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85566-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="85566-122">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85566-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="85566-123">-확인</span><span class="sxs-lookup"><span data-stu-id="85566-123">-Confirm</span></span>
<span data-ttu-id="85566-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85566-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85566-125">-WhatIf</span></span>
<span data-ttu-id="85566-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85566-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85566-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85566-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85566-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85566-128">CommonParameters</span></span>
<span data-ttu-id="85566-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85566-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85566-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85566-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85566-131">입력</span><span class="sxs-lookup"><span data-stu-id="85566-131">INPUTS</span></span>

## <span data-ttu-id="85566-132">출력</span><span class="sxs-lookup"><span data-stu-id="85566-132">OUTPUTS</span></span>

## <span data-ttu-id="85566-133">상속자</span><span class="sxs-lookup"><span data-stu-id="85566-133">NOTES</span></span>

## <span data-ttu-id="85566-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85566-134">RELATED LINKS</span></span>

[<span data-ttu-id="85566-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85566-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="85566-136">새로운 AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85566-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)