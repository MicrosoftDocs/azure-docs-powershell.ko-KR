---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048963"
---
# <span data-ttu-id="beffa-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="beffa-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="beffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beffa-102">SYNOPSIS</span></span>
<span data-ttu-id="beffa-103">ANF (Azure NetApp Files) 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="beffa-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="beffa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="beffa-104">SYNTAX</span></span>

### <span data-ttu-id="beffa-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="beffa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beffa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="beffa-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beffa-107">설명은</span><span class="sxs-lookup"><span data-stu-id="beffa-107">DESCRIPTION</span></span>
<span data-ttu-id="beffa-108">**Get-AzNetAppFilesAccount** cmdlet은 anf 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="beffa-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="beffa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="beffa-109">EXAMPLES</span></span>

### <span data-ttu-id="beffa-110">예제 1: ANF 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="beffa-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="beffa-111">이 명령은 MyAnfAccount 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="beffa-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="beffa-112">변수</span><span class="sxs-lookup"><span data-stu-id="beffa-112">PARAMETERS</span></span>

### <span data-ttu-id="beffa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beffa-113">-DefaultProfile</span></span>
<span data-ttu-id="beffa-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="beffa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beffa-115">-이름</span><span class="sxs-lookup"><span data-stu-id="beffa-115">-Name</span></span>
<span data-ttu-id="beffa-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="beffa-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beffa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beffa-117">-ResourceGroupName</span></span>
<span data-ttu-id="beffa-118">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="beffa-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beffa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="beffa-119">-ResourceId</span></span>
<span data-ttu-id="beffa-120">ANF 계정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="beffa-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beffa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beffa-121">CommonParameters</span></span>
<span data-ttu-id="beffa-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="beffa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beffa-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="beffa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beffa-124">입력</span><span class="sxs-lookup"><span data-stu-id="beffa-124">INPUTS</span></span>

### <span data-ttu-id="beffa-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="beffa-125">System.String</span></span>

## <span data-ttu-id="beffa-126">출력</span><span class="sxs-lookup"><span data-stu-id="beffa-126">OUTPUTS</span></span>

### <span data-ttu-id="beffa-127">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="beffa-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="beffa-128">상속자</span><span class="sxs-lookup"><span data-stu-id="beffa-128">NOTES</span></span>

## <span data-ttu-id="beffa-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="beffa-129">RELATED LINKS</span></span>