---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: d7508f50b39f04894e365ff19b7018ecd4baf445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034209"
---
# <span data-ttu-id="15122-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15122-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="15122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15122-102">SYNOPSIS</span></span>
<span data-ttu-id="15122-103">데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15122-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="15122-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15122-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15122-105">설명은</span><span class="sxs-lookup"><span data-stu-id="15122-105">DESCRIPTION</span></span>
<span data-ttu-id="15122-106">**AzSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15122-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="15122-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 사용 하 여 규칙을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="15122-108">*TableName* 및 *ColumnName* 을 제공 하 여 규칙의 대상을 지정 하 고 *MaskingFunction* 매개 변수를 입력 하 여 데이터 마스크 방법을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="15122-109">*MaskingFunction* 에 Number 또는 text 값이 있으면 숫자 *의 시작* 및 *번호를* 매개 변수로 지정 하거나, 숫자 마스킹 또는 *PrefixSize* , *ReplacementString* , 텍스트 마스킹에 *SuffixSize* 을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15122-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="15122-110">명령이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 cmdlet은 규칙 식별자 외에도 데이터 마스킹 규칙 속성에 대해 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="15122-111">규칙 식별자에는 *ResourceGroupName* , *ServerName* , *DatabaseName* , *RuleID* 이 포함 되지만이에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15122-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="15122-112">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15122-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="15122-113">예제의</span><span class="sxs-lookup"><span data-stu-id="15122-113">EXAMPLES</span></span>

### <span data-ttu-id="15122-114">예제 1: 데이터베이스의 숫자 열에 대 한 데이터 마스킹 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="15122-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="15122-115">이 명령은 Schema01 이라는 스키마의 Table01 테이블에서 Column01 이라는 열에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15122-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="15122-116">Database01 라는 데이터베이스에는 이러한 항목이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15122-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="15122-117">규칙은 5와 14 사이의 난수를 마스크 값으로 사용 하는 숫자 마스킹 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="15122-118">규칙의 이름은 Rule01입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="15122-119">변수</span><span class="sxs-lookup"><span data-stu-id="15122-119">PARAMETERS</span></span>

### <span data-ttu-id="15122-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="15122-120">-ColumnName</span></span>
<span data-ttu-id="15122-121">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="15122-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15122-122">-DatabaseName</span></span>
<span data-ttu-id="15122-123">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="15122-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15122-124">-DefaultProfile</span></span>
<span data-ttu-id="15122-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="15122-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15122-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="15122-126">-MaskingFunction</span></span>
<span data-ttu-id="15122-127">규칙에서 사용 하는 마스킹 기능을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="15122-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="15122-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="15122-129">기본값</span><span class="sxs-lookup"><span data-stu-id="15122-129">Default</span></span>
- <span data-ttu-id="15122-130">NoMasking</span><span class="sxs-lookup"><span data-stu-id="15122-130">NoMasking</span></span>
- <span data-ttu-id="15122-131">본문</span><span class="sxs-lookup"><span data-stu-id="15122-131">Text</span></span>
- <span data-ttu-id="15122-132">숫자로</span><span class="sxs-lookup"><span data-stu-id="15122-132">Number</span></span>
- <span data-ttu-id="15122-133">사회 Alsecurity번호</span><span class="sxs-lookup"><span data-stu-id="15122-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="15122-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="15122-134">CreditCardNumber</span></span>
- <span data-ttu-id="15122-135">전자 메일 기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-135">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-136">-번호</span><span class="sxs-lookup"><span data-stu-id="15122-136">-NumberFrom</span></span>
<span data-ttu-id="15122-137">임의의 값이 선택 되는 간격의 하한값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="15122-138">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15122-139">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-139">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-140">-번호를</span><span class="sxs-lookup"><span data-stu-id="15122-140">-NumberTo</span></span>
<span data-ttu-id="15122-141">임의 값이 선택 된 간격의 상한 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="15122-142">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15122-143">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-143">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15122-144">-PassThru</span></span>
<span data-ttu-id="15122-145">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15122-146">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15122-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15122-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="15122-147">-PrefixSize</span></span>
<span data-ttu-id="15122-148">마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="15122-149">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15122-150">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-150">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="15122-151">-ReplacementString</span></span>
<span data-ttu-id="15122-152">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="15122-153">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15122-154">기본값은 빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-154">The default value is an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15122-155">-ResourceGroupName</span></span>
<span data-ttu-id="15122-156">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="15122-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="15122-157">-SchemaName</span></span>
<span data-ttu-id="15122-158">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="15122-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15122-159">-ServerName</span></span>
<span data-ttu-id="15122-160">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="15122-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="15122-161">-SuffixSize</span></span>
<span data-ttu-id="15122-162">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="15122-163">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15122-164">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="15122-164">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15122-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="15122-165">-TableName</span></span>
<span data-ttu-id="15122-166">마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="15122-167">-확인</span><span class="sxs-lookup"><span data-stu-id="15122-167">-Confirm</span></span>
<span data-ttu-id="15122-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15122-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15122-169">-WhatIf</span></span>
<span data-ttu-id="15122-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15122-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15122-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15122-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15122-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15122-172">CommonParameters</span></span>
<span data-ttu-id="15122-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15122-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15122-174">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15122-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15122-175">입력</span><span class="sxs-lookup"><span data-stu-id="15122-175">INPUTS</span></span>

### <span data-ttu-id="15122-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15122-176">System.String</span></span>

### <span data-ttu-id="15122-177">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15122-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="15122-178">시스템 Null 허용 ' 1 [[4.0.0.0] [[System.webserver, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15122-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="15122-179">출력</span><span class="sxs-lookup"><span data-stu-id="15122-179">OUTPUTS</span></span>

### <span data-ttu-id="15122-180">DataMasking. DatabaseDataMaskingRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="15122-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="15122-181">상속자</span><span class="sxs-lookup"><span data-stu-id="15122-181">NOTES</span></span>

## <span data-ttu-id="15122-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15122-182">RELATED LINKS</span></span>

[<span data-ttu-id="15122-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15122-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15122-184">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15122-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15122-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15122-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15122-186">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="15122-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

