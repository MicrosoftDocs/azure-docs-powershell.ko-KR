---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204261"
---
# <span data-ttu-id="9b3ca-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="9b3ca-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="9b3ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3ca-103">새 sql 가상 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="9b3ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b3ca-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3ca-106">New-AzSqlVMGroup cmdlet은 Azure SQL 가상 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="9b3ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b3ca-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3ca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b3ca-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="9b3ca-109">리소스 그룹 ResourceGroup01에서 테스트 그룹 vm을 사용 하 여 새 Azure SQL 가상 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="9b3ca-110">$profile는 WsfcDomainProfile 형식의 개체입니다. SqlVirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="9b3ca-111">변수</span><span class="sxs-lookup"><span data-stu-id="9b3ca-111">PARAMETERS</span></span>

### <span data-ttu-id="9b3ca-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b3ca-112">-AsJob</span></span>
<span data-ttu-id="9b3ca-113">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9b3ca-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="9b3ca-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="9b3ca-115">클러스터를 만드는 데 사용 된 이름</span><span class="sxs-lookup"><span data-stu-id="9b3ca-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="9b3ca-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="9b3ca-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="9b3ca-117">운영 클러스터에 사용 되는 이름</span><span class="sxs-lookup"><span data-stu-id="9b3ca-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="9b3ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ca-118">-DefaultProfile</span></span>
<span data-ttu-id="9b3ca-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3ca-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="9b3ca-120">-DomainFqdn</span></span>
<span data-ttu-id="9b3ca-121">도메인의 정규화 된 이름</span><span class="sxs-lookup"><span data-stu-id="9b3ca-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="9b3ca-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="9b3ca-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="9b3ca-123">공유 서버 감시의 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="9b3ca-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="9b3ca-124">-위치</span><span class="sxs-lookup"><span data-stu-id="9b3ca-124">-Location</span></span>
<span data-ttu-id="9b3ca-125">SQL 가상 컴퓨터 그룹 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3ca-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9b3ca-126">-Name</span></span>
<span data-ttu-id="9b3ca-127">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3ca-128">-제공</span><span class="sxs-lookup"><span data-stu-id="9b3ca-128">-Offer</span></span>
<span data-ttu-id="9b3ca-129">SQL 가상 컴퓨터 그룹 제안.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="9b3ca-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="9b3ca-130">-OuPath</span></span>
<span data-ttu-id="9b3ca-131">노드 및 클러스터가 표시 될 조직 구성 단위 경로</span><span class="sxs-lookup"><span data-stu-id="9b3ca-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="9b3ca-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3ca-132">-ResourceGroupName</span></span>
<span data-ttu-id="9b3ca-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3ca-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="9b3ca-134">-Sku</span></span>
<span data-ttu-id="9b3ca-135">SQL 가상 컴퓨터 그룹 에디션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="9b3ca-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="9b3ca-136">-SqlServiceAccount</span></span>
<span data-ttu-id="9b3ca-137">클러스터의 모든 참여 SQL 가상 컴퓨터에서 SQL 서비스를 실행할 때 사용할 수 있는 이름</span><span class="sxs-lookup"><span data-stu-id="9b3ca-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="9b3ca-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9b3ca-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="9b3ca-139">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="9b3ca-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3ca-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="9b3ca-140">-StorageAccountUrl</span></span>
<span data-ttu-id="9b3ca-141">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="9b3ca-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="9b3ca-142">태그</span><span class="sxs-lookup"><span data-stu-id="9b3ca-142">-Tag</span></span>
<span data-ttu-id="9b3ca-143">SQL 가상 컴퓨터 그룹과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3ca-144">-확인</span><span class="sxs-lookup"><span data-stu-id="9b3ca-144">-Confirm</span></span>
<span data-ttu-id="9b3ca-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3ca-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3ca-146">-WhatIf</span></span>
<span data-ttu-id="9b3ca-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3ca-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3ca-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3ca-149">CommonParameters</span></span>
<span data-ttu-id="9b3ca-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3ca-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b3ca-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3ca-152">입력</span><span class="sxs-lookup"><span data-stu-id="9b3ca-152">INPUTS</span></span>

### <span data-ttu-id="9b3ca-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b3ca-153">System.String</span></span>

## <span data-ttu-id="9b3ca-154">출력</span><span class="sxs-lookup"><span data-stu-id="9b3ca-154">OUTPUTS</span></span>

### <span data-ttu-id="9b3ca-155">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="9b3ca-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="9b3ca-156">상속자</span><span class="sxs-lookup"><span data-stu-id="9b3ca-156">NOTES</span></span>

## <span data-ttu-id="9b3ca-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b3ca-157">RELATED LINKS</span></span>