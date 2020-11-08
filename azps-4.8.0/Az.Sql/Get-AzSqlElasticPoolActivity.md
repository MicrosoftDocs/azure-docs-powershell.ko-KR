---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048683"
---
# <span data-ttu-id="27f2d-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="27f2d-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="27f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="27f2d-103">탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="27f2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27f2d-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27f2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="27f2d-106">**AzSqlElasticPoolActivity** Cmdlet은 Azure SQL 데이터베이스의 탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="27f2d-107">풀 만들기 및 구성 업데이트의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="27f2d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="27f2d-108">EXAMPLES</span></span>

### <span data-ttu-id="27f2d-109">예제 1: 탄력적 풀에 대 한 작업 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="27f2d-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="27f2d-110">이 명령은 ElasticPool01 이라는 탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="27f2d-111">변수</span><span class="sxs-lookup"><span data-stu-id="27f2d-111">PARAMETERS</span></span>

### <span data-ttu-id="27f2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f2d-112">-DefaultProfile</span></span>
<span data-ttu-id="27f2d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="27f2d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27f2d-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="27f2d-114">-ElasticPoolName</span></span>
<span data-ttu-id="27f2d-115">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-115">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f2d-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="27f2d-116">-OperationId</span></span>
<span data-ttu-id="27f2d-117">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f2d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27f2d-118">-ResourceGroupName</span></span>
<span data-ttu-id="27f2d-119">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="27f2d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27f2d-120">-ServerName</span></span>
<span data-ttu-id="27f2d-121">탄력적 풀이 포함 된 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="27f2d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="27f2d-122">-Confirm</span></span>
<span data-ttu-id="27f2d-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27f2d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27f2d-124">-WhatIf</span></span>
<span data-ttu-id="27f2d-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27f2d-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27f2d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f2d-127">CommonParameters</span></span>
<span data-ttu-id="27f2d-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f2d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f2d-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27f2d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f2d-130">입력</span><span class="sxs-lookup"><span data-stu-id="27f2d-130">INPUTS</span></span>

### <span data-ttu-id="27f2d-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27f2d-131">System.String</span></span>

### <span data-ttu-id="27f2d-132">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27f2d-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="27f2d-133">출력</span><span class="sxs-lookup"><span data-stu-id="27f2d-133">OUTPUTS</span></span>

### <span data-ttu-id="27f2d-134">ElasticPool. AzureSqlElasticPoolActivityModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="27f2d-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="27f2d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="27f2d-135">NOTES</span></span>

## <span data-ttu-id="27f2d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27f2d-136">RELATED LINKS</span></span>

[<span data-ttu-id="27f2d-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27f2d-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="27f2d-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="27f2d-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="27f2d-139">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27f2d-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="27f2d-140">제거-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27f2d-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="27f2d-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27f2d-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

