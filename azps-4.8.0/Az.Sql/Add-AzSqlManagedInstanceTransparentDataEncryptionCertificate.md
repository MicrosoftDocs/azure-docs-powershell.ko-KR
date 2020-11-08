---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204833"
---
# <span data-ttu-id="d27b8-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d27b8-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="d27b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d27b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d27b8-103">지정 된 관리 되는 인스턴스에 대 한 투명 한 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="d27b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d27b8-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d27b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d27b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d27b8-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate는 지정 된 관리 인스턴스에 대 한 투명 한 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="d27b8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d27b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d27b8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d27b8-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="d27b8-109">변수</span><span class="sxs-lookup"><span data-stu-id="d27b8-109">PARAMETERS</span></span>

### <span data-ttu-id="d27b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27b8-110">-DefaultProfile</span></span>
<span data-ttu-id="d27b8-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27b8-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="d27b8-112">-ManagedInstanceName</span></span>
<span data-ttu-id="d27b8-113">관리 되는 인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="d27b8-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27b8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d27b8-114">-PassThru</span></span>
<span data-ttu-id="d27b8-115">성공적으로 실행 되 면 추가 된 인증서 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="d27b8-116">-암호</span><span class="sxs-lookup"><span data-stu-id="d27b8-116">-Password</span></span>
<span data-ttu-id="d27b8-117">투명 한 데이터 암호화 인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="d27b8-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27b8-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="d27b8-118">-PrivateBlob</span></span>
<span data-ttu-id="d27b8-119">투명 한 데이터 암호화 인증서 용 개인 blob</span><span class="sxs-lookup"><span data-stu-id="d27b8-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d27b8-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d27b8-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="d27b8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="d27b8-122">-Confirm</span></span>
<span data-ttu-id="d27b8-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d27b8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d27b8-124">-WhatIf</span></span>
<span data-ttu-id="d27b8-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27b8-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d27b8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27b8-127">CommonParameters</span></span>
<span data-ttu-id="d27b8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27b8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27b8-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d27b8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27b8-130">입력</span><span class="sxs-lookup"><span data-stu-id="d27b8-130">INPUTS</span></span>

### <span data-ttu-id="d27b8-131">않아야</span><span class="sxs-lookup"><span data-stu-id="d27b8-131">None</span></span>

## <span data-ttu-id="d27b8-132">출력</span><span class="sxs-lookup"><span data-stu-id="d27b8-132">OUTPUTS</span></span>

### <span data-ttu-id="d27b8-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d27b8-133">System.Boolean</span></span>

## <span data-ttu-id="d27b8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d27b8-134">NOTES</span></span>

## <span data-ttu-id="d27b8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d27b8-135">RELATED LINKS</span></span>