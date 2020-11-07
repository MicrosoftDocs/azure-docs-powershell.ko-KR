---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 6e9aa41b30b9a2012e4208971ceddff8f08e980a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876806"
---
# <span data-ttu-id="35a74-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="35a74-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="35a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a74-102">SYNOPSIS</span></span>
<span data-ttu-id="35a74-103">장치에 대 한 새 순서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="35a74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35a74-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a74-105">설명은</span><span class="sxs-lookup"><span data-stu-id="35a74-105">DESCRIPTION</span></span>
<span data-ttu-id="35a74-106">**AzDataBoxEdgeOrder** Cmdlet은 데이터 상자 가장자리 장치에 대 한 새 순서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="35a74-107">주문을 만들기 전에 데이터 상자 가장자리 장치 리소스를 먼저 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="35a74-108">연락처, 회사 이름, 전자 메일, 주소 등과 같은 세부 정보를 주문 만들기에 대 한 매개 변수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="35a74-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35a74-109">EXAMPLES</span></span>

### <span data-ttu-id="35a74-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="35a74-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="35a74-111">변수</span><span class="sxs-lookup"><span data-stu-id="35a74-111">PARAMETERS</span></span>

### <span data-ttu-id="35a74-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="35a74-112">-AddressLine1</span></span>
<span data-ttu-id="35a74-113">주소 첫 줄</span><span class="sxs-lookup"><span data-stu-id="35a74-113">Address first line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="35a74-114">-AddressLine2</span></span>
<span data-ttu-id="35a74-115">주소 2 줄</span><span class="sxs-lookup"><span data-stu-id="35a74-115">Address second line</span></span>

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

### <span data-ttu-id="35a74-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="35a74-116">-AddressLine3</span></span>
<span data-ttu-id="35a74-117">주소 3 라인</span><span class="sxs-lookup"><span data-stu-id="35a74-117">Address third line</span></span>

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

### <span data-ttu-id="35a74-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35a74-118">-AsJob</span></span>
<span data-ttu-id="35a74-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="35a74-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35a74-120">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="35a74-120">-City</span></span>
<span data-ttu-id="35a74-121">구/군/시 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-121">Name of the City</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="35a74-122">-CompanyName</span></span>
<span data-ttu-id="35a74-123">회사 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-123">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-124">-연락처 사용자</span><span class="sxs-lookup"><span data-stu-id="35a74-124">-ContactPerson</span></span>
<span data-ttu-id="35a74-125">연락처의 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-125">Name of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-126">-국가</span><span class="sxs-lookup"><span data-stu-id="35a74-126">-Country</span></span>
<span data-ttu-id="35a74-127">국가 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-127">Name of the Country</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a74-128">-DefaultProfile</span></span>
<span data-ttu-id="35a74-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a74-130">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-130">-DeviceName</span></span>
<span data-ttu-id="35a74-131">자원 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-131">Resource Name</span></span>

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

### <span data-ttu-id="35a74-132">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="35a74-132">-Email</span></span>
<span data-ttu-id="35a74-133">업데이트를 받을 전자 메일 목록, 최대 10 개의 전자 메일 수락</span><span class="sxs-lookup"><span data-stu-id="35a74-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-134">-전화</span><span class="sxs-lookup"><span data-stu-id="35a74-134">-Phone</span></span>
<span data-ttu-id="35a74-135">담당자의 전화 번호</span><span class="sxs-lookup"><span data-stu-id="35a74-135">Phone number of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="35a74-136">-PostalCode</span></span>
<span data-ttu-id="35a74-137">주소의 우편 번호</span><span class="sxs-lookup"><span data-stu-id="35a74-137">Postal Code of the Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a74-138">-ResourceGroupName</span></span>
<span data-ttu-id="35a74-139">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="35a74-139">Resource Group Name</span></span>

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

### <span data-ttu-id="35a74-140">-상태</span><span class="sxs-lookup"><span data-stu-id="35a74-140">-State</span></span>
<span data-ttu-id="35a74-141">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-141">Name of the State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-142">-확인</span><span class="sxs-lookup"><span data-stu-id="35a74-142">-Confirm</span></span>
<span data-ttu-id="35a74-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a74-144">-WhatIf</span></span>
<span data-ttu-id="35a74-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35a74-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a74-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a74-147">CommonParameters</span></span>
<span data-ttu-id="35a74-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a74-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a74-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35a74-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a74-150">입력</span><span class="sxs-lookup"><span data-stu-id="35a74-150">INPUTS</span></span>

### <span data-ttu-id="35a74-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35a74-151">System.String</span></span>

## <span data-ttu-id="35a74-152">출력</span><span class="sxs-lookup"><span data-stu-id="35a74-152">OUTPUTS</span></span>

### <span data-ttu-id="35a74-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="35a74-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="35a74-154">상속자</span><span class="sxs-lookup"><span data-stu-id="35a74-154">NOTES</span></span>

## <span data-ttu-id="35a74-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35a74-155">RELATED LINKS</span></span>