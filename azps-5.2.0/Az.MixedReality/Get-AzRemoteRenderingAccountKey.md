---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328138"
---
# <span data-ttu-id="52173-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="52173-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="52173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52173-102">SYNOPSIS</span></span>
<span data-ttu-id="52173-103">원격 렌더링 계정의 키 얻기</span><span class="sxs-lookup"><span data-stu-id="52173-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="52173-104">구문</span><span class="sxs-lookup"><span data-stu-id="52173-104">SYNTAX</span></span>

### <span data-ttu-id="52173-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="52173-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52173-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52173-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52173-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="52173-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52173-108">설명</span><span class="sxs-lookup"><span data-stu-id="52173-108">DESCRIPTION</span></span>
<span data-ttu-id="52173-109">원격 렌더링 계정의 개발자 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52173-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="52173-110">예제</span><span class="sxs-lookup"><span data-stu-id="52173-110">EXAMPLES</span></span>

### <span data-ttu-id="52173-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="52173-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="52173-112">현재 구독 및 리소스 그룹 "rg1"에서 원격 렌더링 계정 "example"의 개발자 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52173-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="52173-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="52173-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="52173-114">현재 구독에서 원격 렌더링 계정 "example"의 개발자 키를, 파이핑을 사용하여 리소스 그룹 "rg1"을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52173-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="52173-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52173-115">PARAMETERS</span></span>

### <span data-ttu-id="52173-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52173-116">-DefaultProfile</span></span>
<span data-ttu-id="52173-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52173-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52173-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52173-118">-InputObject</span></span>
<span data-ttu-id="52173-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="52173-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52173-120">-Name</span><span class="sxs-lookup"><span data-stu-id="52173-120">-Name</span></span>
<span data-ttu-id="52173-121">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52173-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52173-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52173-122">-ResourceGroupName</span></span>
<span data-ttu-id="52173-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52173-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52173-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52173-124">-ResourceId</span></span>
<span data-ttu-id="52173-125">원격 렌더링 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="52173-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52173-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52173-126">CommonParameters</span></span>
<span data-ttu-id="52173-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52173-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="52173-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="52173-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52173-129">입력</span><span class="sxs-lookup"><span data-stu-id="52173-129">INPUTS</span></span>

### <span data-ttu-id="52173-130">System.String</span><span class="sxs-lookup"><span data-stu-id="52173-130">System.String</span></span>

### <span data-ttu-id="52173-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="52173-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="52173-132">출력</span><span class="sxs-lookup"><span data-stu-id="52173-132">OUTPUTS</span></span>

### <span data-ttu-id="52173-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="52173-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="52173-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52173-134">NOTES</span></span>

## <span data-ttu-id="52173-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52173-135">RELATED LINKS</span></span>