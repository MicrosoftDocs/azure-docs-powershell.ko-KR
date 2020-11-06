---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527192"
---
# <span data-ttu-id="ce1b1-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce1b1-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ce1b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1b1-103">데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce1b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce1b1-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce1b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce1b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ce1b1-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="ce1b1-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 제공 하 여 규칙을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="ce1b1-108">*SchemaName* , *TableName* , *ColumnName* 의 매개 변수를 제공 하 여 규칙의 대상을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="ce1b1-109">*MaskingFunction* 매개 변수를 지정 하 여 데이터 마스크 방법을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="ce1b1-110">Number 또는 *MaskingFunction* 에 대 한 텍스트 값을 지정 *하는 경우* 숫자 마스킹에 대 한 매개 변수 및 번호 *를* 지정할 수 있으며, 텍스트 마스킹에 대 한 *PrefixSize* , *ReplacementString* 및 *SuffixSize* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="ce1b1-111">명령이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="ce1b1-112">규칙 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** , **RuleId** 이 포함 되지만이에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="ce1b1-113">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ce1b1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="ce1b1-114">EXAMPLES</span></span>

### <span data-ttu-id="ce1b1-115">예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경</span><span class="sxs-lookup"><span data-stu-id="ce1b1-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="ce1b1-116">이 명령은 ID Rule17 인 데이터 마스킹 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="ce1b1-117">이 규칙은 서버 Server01의 Database01 라는 데이터베이스에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="ce1b1-118">이 명령은 임의의 숫자가 마스킹된 값으로 생성 되는 간격의 경계를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="ce1b1-119">새 범위는 23 ~ 42입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="ce1b1-120">변수</span><span class="sxs-lookup"><span data-stu-id="ce1b1-120">PARAMETERS</span></span>

### <span data-ttu-id="ce1b1-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-121">-ColumnName</span></span>
<span data-ttu-id="ce1b1-122">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="ce1b1-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-123">-DatabaseName</span></span>
<span data-ttu-id="ce1b1-124">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ce1b1-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="ce1b1-125">-MaskingFunction</span></span>
<span data-ttu-id="ce1b1-126">규칙에서 사용 하는 마스킹 기능을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="ce1b1-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce1b1-128">기본값</span><span class="sxs-lookup"><span data-stu-id="ce1b1-128">Default</span></span>
- <span data-ttu-id="ce1b1-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="ce1b1-129">NoMasking</span></span>
- <span data-ttu-id="ce1b1-130">본문</span><span class="sxs-lookup"><span data-stu-id="ce1b1-130">Text</span></span>
- <span data-ttu-id="ce1b1-131">숫자로</span><span class="sxs-lookup"><span data-stu-id="ce1b1-131">Number</span></span>
- <span data-ttu-id="ce1b1-132">사회 Alsecurity번호</span><span class="sxs-lookup"><span data-stu-id="ce1b1-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="ce1b1-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="ce1b1-133">CreditCardNumber</span></span>
- <span data-ttu-id="ce1b1-134">메일 주소</span><span class="sxs-lookup"><span data-stu-id="ce1b1-134">Email</span></span>

<span data-ttu-id="ce1b1-135">기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-135">The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b1-136">-번호</span><span class="sxs-lookup"><span data-stu-id="ce1b1-136">-NumberFrom</span></span>
<span data-ttu-id="ce1b1-137">임의의 값이 선택 되는 간격의 하한값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ce1b1-138">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce1b1-139">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-139">The default value is 0.</span></span>

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

### <span data-ttu-id="ce1b1-140">-번호를</span><span class="sxs-lookup"><span data-stu-id="ce1b1-140">-NumberTo</span></span>
<span data-ttu-id="ce1b1-141">임의 값이 선택 된 간격의 상한 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ce1b1-142">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce1b1-143">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-143">The default value is 0.</span></span>

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

### <span data-ttu-id="ce1b1-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce1b1-144">-PassThru</span></span>
<span data-ttu-id="ce1b1-145">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce1b1-146">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce1b1-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="ce1b1-147">-PrefixSize</span></span>
<span data-ttu-id="ce1b1-148">마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="ce1b1-149">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce1b1-150">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-150">The default value is 0.</span></span>

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

### <span data-ttu-id="ce1b1-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="ce1b1-151">-ReplacementString</span></span>
<span data-ttu-id="ce1b1-152">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ce1b1-153">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce1b1-154">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-154">The default value is 0.</span></span>

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

### <span data-ttu-id="ce1b1-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-155">-ResourceGroupName</span></span>
<span data-ttu-id="ce1b1-156">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ce1b1-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-157">-SchemaName</span></span>
<span data-ttu-id="ce1b1-158">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="ce1b1-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-159">-ServerName</span></span>
<span data-ttu-id="ce1b1-160">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ce1b1-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="ce1b1-161">-SuffixSize</span></span>
<span data-ttu-id="ce1b1-162">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ce1b1-163">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce1b1-164">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-164">The default value is 0.</span></span>

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

### <span data-ttu-id="ce1b1-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="ce1b1-165">-TableName</span></span>
<span data-ttu-id="ce1b1-166">마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="ce1b1-167">-확인</span><span class="sxs-lookup"><span data-stu-id="ce1b1-167">-Confirm</span></span>
<span data-ttu-id="ce1b1-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce1b1-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce1b1-169">-WhatIf</span></span>
<span data-ttu-id="ce1b1-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce1b1-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce1b1-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1b1-172">-DefaultProfile</span></span>
<span data-ttu-id="ce1b1-173">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce1b1-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1b1-174">CommonParameters</span></span>
<span data-ttu-id="ce1b1-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1b1-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce1b1-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1b1-177">입력</span><span class="sxs-lookup"><span data-stu-id="ce1b1-177">INPUTS</span></span>

###  
<span data-ttu-id="ce1b1-178">않아야</span><span class="sxs-lookup"><span data-stu-id="ce1b1-178">None</span></span>

## <span data-ttu-id="ce1b1-179">출력</span><span class="sxs-lookup"><span data-stu-id="ce1b1-179">OUTPUTS</span></span>

### <span data-ttu-id="ce1b1-180">DatabaseDataMaskingRuleModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="ce1b1-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ce1b1-181">상속자</span><span class="sxs-lookup"><span data-stu-id="ce1b1-181">NOTES</span></span>

## <span data-ttu-id="ce1b1-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce1b1-182">RELATED LINKS</span></span>

[<span data-ttu-id="ce1b1-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce1b1-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce1b1-184">새로운 AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce1b1-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce1b1-185">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce1b1-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce1b1-186">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ce1b1-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

