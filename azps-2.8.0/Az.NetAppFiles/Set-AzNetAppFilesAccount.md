---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: 873b506ea1fd50e2869a19a45a302c5fe12a781b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870929"
---
# <span data-ttu-id="38ed4-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="38ed4-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="38ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="38ed4-103">새 데이터 집합을 사용 하 여 Azure NetApp Files (ANF) 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="38ed4-104">관련 된 active directory를 삭제 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="38ed4-105">구문과</span><span class="sxs-lookup"><span data-stu-id="38ed4-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ed4-106">설명은</span><span class="sxs-lookup"><span data-stu-id="38ed4-106">DESCRIPTION</span></span>
<span data-ttu-id="38ed4-107">**Set-AzNetAppFilesAccount** cmdlet은 anf 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="38ed4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="38ed4-108">EXAMPLES</span></span>

### <span data-ttu-id="38ed4-109">예제 1: ANF 계정 수정</span><span class="sxs-lookup"><span data-stu-id="38ed4-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="38ed4-110">이 명령은 지정 된 계정에 대 한 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-110">This command performs an update on the given account.</span></span> <span data-ttu-id="38ed4-111">Active directory가 없으면 계정에서 제거 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="38ed4-112">변수</span><span class="sxs-lookup"><span data-stu-id="38ed4-112">PARAMETERS</span></span>

### <span data-ttu-id="38ed4-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="38ed4-113">-ActiveDirectories</span></span>
<span data-ttu-id="38ed4-114">Active directory를 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="38ed4-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ed4-115">-DefaultProfile</span></span>
<span data-ttu-id="38ed4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ed4-117">-위치</span><span class="sxs-lookup"><span data-stu-id="38ed4-117">-Location</span></span>
<span data-ttu-id="38ed4-118">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="38ed4-118">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="38ed4-119">-Name</span></span>
<span data-ttu-id="38ed4-120">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="38ed4-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ed4-121">-ResourceGroupName</span></span>
<span data-ttu-id="38ed4-122">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="38ed4-122">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-123">태그</span><span class="sxs-lookup"><span data-stu-id="38ed4-123">-Tag</span></span>
<span data-ttu-id="38ed4-124">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="38ed4-124">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-125">-확인</span><span class="sxs-lookup"><span data-stu-id="38ed4-125">-Confirm</span></span>
<span data-ttu-id="38ed4-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ed4-127">-WhatIf</span></span>
<span data-ttu-id="38ed4-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ed4-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ed4-130">CommonParameters</span></span>
<span data-ttu-id="38ed4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ed4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38ed4-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ed4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ed4-133">입력</span><span class="sxs-lookup"><span data-stu-id="38ed4-133">INPUTS</span></span>

### <span data-ttu-id="38ed4-134">않아야</span><span class="sxs-lookup"><span data-stu-id="38ed4-134">None</span></span>

## <span data-ttu-id="38ed4-135">출력</span><span class="sxs-lookup"><span data-stu-id="38ed4-135">OUTPUTS</span></span>

### <span data-ttu-id="38ed4-136">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="38ed4-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="38ed4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="38ed4-137">NOTES</span></span>

## <span data-ttu-id="38ed4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38ed4-138">RELATED LINKS</span></span>