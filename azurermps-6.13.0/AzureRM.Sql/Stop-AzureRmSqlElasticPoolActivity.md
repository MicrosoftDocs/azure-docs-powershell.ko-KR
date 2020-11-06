---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529323"
---
# <span data-ttu-id="72870-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="72870-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="72870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72870-102">SYNOPSIS</span></span>
<span data-ttu-id="72870-103">탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="72870-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72870-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72870-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72870-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72870-105">DESCRIPTION</span></span>
<span data-ttu-id="72870-106">**AzureRmSqlElasticPoolActivity** cmdlet은 탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="72870-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="72870-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72870-107">EXAMPLES</span></span>

### <span data-ttu-id="72870-108">예제 1: 탄력적 풀에서 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="72870-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="72870-109">이 명령은 탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="72870-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="72870-110">변수</span><span class="sxs-lookup"><span data-stu-id="72870-110">PARAMETERS</span></span>

### <span data-ttu-id="72870-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72870-111">-DefaultProfile</span></span>
<span data-ttu-id="72870-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72870-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72870-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="72870-113">-ElasticPoolName</span></span>
<span data-ttu-id="72870-114">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72870-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="72870-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="72870-115">-OperationId</span></span>
<span data-ttu-id="72870-116">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72870-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="72870-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72870-117">-PassThru</span></span>
<span data-ttu-id="72870-118">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="72870-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72870-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72870-119">-ResourceGroupName</span></span>
<span data-ttu-id="72870-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72870-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="72870-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72870-121">-ServerName</span></span>
<span data-ttu-id="72870-122">탄력적인 풀이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72870-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="72870-123">-확인</span><span class="sxs-lookup"><span data-stu-id="72870-123">-Confirm</span></span>
<span data-ttu-id="72870-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72870-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72870-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72870-125">-WhatIf</span></span>
<span data-ttu-id="72870-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72870-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72870-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72870-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72870-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72870-128">CommonParameters</span></span>
<span data-ttu-id="72870-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72870-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72870-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72870-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72870-131">입력</span><span class="sxs-lookup"><span data-stu-id="72870-131">INPUTS</span></span>

### <span data-ttu-id="72870-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72870-132">System.String</span></span>

### <span data-ttu-id="72870-133">시스템 Null 허용 ' 1 [[b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="72870-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="72870-134">출력</span><span class="sxs-lookup"><span data-stu-id="72870-134">OUTPUTS</span></span>

### <span data-ttu-id="72870-135">ElasticPool. AzureSqlElasticPoolActivityModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="72870-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="72870-136">상속자</span><span class="sxs-lookup"><span data-stu-id="72870-136">NOTES</span></span>

## <span data-ttu-id="72870-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72870-137">RELATED LINKS</span></span>