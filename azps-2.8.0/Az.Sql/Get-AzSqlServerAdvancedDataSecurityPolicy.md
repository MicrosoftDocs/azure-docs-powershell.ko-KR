---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 74956ff74beeb166a7788d0e577a86a4d2538ded
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873647"
---
# <span data-ttu-id="b2ab6-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b2ab6-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b2ab6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ab6-103">서버의 고급 데이터 보안 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b2ab6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2ab6-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2ab6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2ab6-105">DESCRIPTION</span></span>
<span data-ttu-id="b2ab6-106">**Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet은 서버의 고급 데이터 보안 정책을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b2ab6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b2ab6-107">EXAMPLES</span></span>

### <span data-ttu-id="b2ab6-108">예제 1-서버 고급 데이터 보안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="b2ab6-109">예제 2-서버 리소스에서 서버 고급 데이터 보안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="b2ab6-110">변수</span><span class="sxs-lookup"><span data-stu-id="b2ab6-110">PARAMETERS</span></span>

### <span data-ttu-id="b2ab6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ab6-111">-DefaultProfile</span></span>
<span data-ttu-id="b2ab6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ab6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2ab6-113">-InputObject</span></span>
<span data-ttu-id="b2ab6-114">고급 데이터 보안 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="b2ab6-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ab6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ab6-115">-ResourceGroupName</span></span>
<span data-ttu-id="b2ab6-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ab6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b2ab6-117">-ServerName</span></span>
<span data-ttu-id="b2ab6-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-118">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ab6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ab6-119">CommonParameters</span></span>
<span data-ttu-id="b2ab6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ab6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2ab6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ab6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ab6-122">입력</span><span class="sxs-lookup"><span data-stu-id="b2ab6-122">INPUTS</span></span>

### <span data-ttu-id="b2ab6-123">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="b2ab6-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b2ab6-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2ab6-124">System.String</span></span>

## <span data-ttu-id="b2ab6-125">출력</span><span class="sxs-lookup"><span data-stu-id="b2ab6-125">OUTPUTS</span></span>

### <span data-ttu-id="b2ab6-126">AdvancedThreatProtection. ServerAdvancedDataSecurityPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="b2ab6-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b2ab6-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b2ab6-127">NOTES</span></span>

## <span data-ttu-id="b2ab6-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2ab6-128">RELATED LINKS</span></span>