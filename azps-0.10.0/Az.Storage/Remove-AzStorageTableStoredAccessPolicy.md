---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 96c6d80f4281b8d3e10d29a288787ff9ebcc5586
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876217"
---
# <span data-ttu-id="aa256-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa256-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="aa256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa256-102">SYNOPSIS</span></span>
<span data-ttu-id="aa256-103">Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="aa256-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa256-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa256-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa256-105">DESCRIPTION</span></span>
<span data-ttu-id="aa256-106">**AzStorageTableStoredAccessPolicy** Cmdlet은 Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="aa256-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa256-107">EXAMPLES</span></span>

### <span data-ttu-id="aa256-108">예제 1: 저장소 테이블에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="aa256-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="aa256-109">이 명령은 MyTable 이라는 저장소 테이블에서 Policy05 이라는 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="aa256-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa256-110">PARAMETERS</span></span>

### <span data-ttu-id="aa256-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="aa256-111">-Context</span></span>
<span data-ttu-id="aa256-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aa256-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa256-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa256-114">-DefaultProfile</span></span>
<span data-ttu-id="aa256-115">Azure와 통신 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-115">communication with Azure.</span></span>

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

### <span data-ttu-id="aa256-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa256-116">-PassThru</span></span>
<span data-ttu-id="aa256-117">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="aa256-118">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="aa256-119">-정책</span><span class="sxs-lookup"><span data-stu-id="aa256-119">-Policy</span></span>
<span data-ttu-id="aa256-120">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa256-121">-테이블</span><span class="sxs-lookup"><span data-stu-id="aa256-121">-Table</span></span>
<span data-ttu-id="aa256-122">Azure 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa256-123">-확인</span><span class="sxs-lookup"><span data-stu-id="aa256-123">-Confirm</span></span>
<span data-ttu-id="aa256-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa256-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa256-125">-WhatIf</span></span>
<span data-ttu-id="aa256-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa256-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa256-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa256-128">CommonParameters</span></span>
<span data-ttu-id="aa256-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa256-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa256-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa256-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa256-131">입력</span><span class="sxs-lookup"><span data-stu-id="aa256-131">INPUTS</span></span>

### <span data-ttu-id="aa256-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa256-132">System.String</span></span>

### <span data-ttu-id="aa256-133">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa256-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aa256-134">출력</span><span class="sxs-lookup"><span data-stu-id="aa256-134">OUTPUTS</span></span>

### <span data-ttu-id="aa256-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aa256-135">System.Boolean</span></span>

## <span data-ttu-id="aa256-136">상속자</span><span class="sxs-lookup"><span data-stu-id="aa256-136">NOTES</span></span>

## <span data-ttu-id="aa256-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa256-137">RELATED LINKS</span></span>

[<span data-ttu-id="aa256-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa256-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="aa256-139">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa256-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="aa256-140">새로운 AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa256-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="aa256-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa256-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)