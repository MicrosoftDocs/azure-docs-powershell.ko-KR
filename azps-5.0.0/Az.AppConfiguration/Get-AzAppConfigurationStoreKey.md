---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216140"
---
# <span data-ttu-id="79c3c-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="79c3c-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="79c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="79c3c-103">지정 된 구성 저장소에 대 한 선택 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="79c3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79c3c-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79c3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="79c3c-106">지정 된 구성 저장소에 대 한 선택 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="79c3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="79c3c-108">예제 1: 앱 구성 저장소의 모든 스토어 키 나열</span><span class="sxs-lookup"><span data-stu-id="79c3c-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="79c3c-109">이 명령은 앱 구성 저장소의 모든 저장소 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="79c3c-110">변수</span><span class="sxs-lookup"><span data-stu-id="79c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="79c3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c3c-111">-DefaultProfile</span></span>
<span data-ttu-id="79c3c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c3c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="79c3c-113">-Name</span></span>
<span data-ttu-id="79c3c-114">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="79c3c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c3c-115">-ResourceGroupName</span></span>
<span data-ttu-id="79c3c-116">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="79c3c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79c3c-117">-SubscriptionId</span></span>
<span data-ttu-id="79c3c-118">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c3c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="79c3c-119">-Confirm</span></span>
<span data-ttu-id="79c3c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c3c-121">-WhatIf</span></span>
<span data-ttu-id="79c3c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c3c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c3c-124">CommonParameters</span></span>
<span data-ttu-id="79c3c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79c3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c3c-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79c3c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c3c-127">입력</span><span class="sxs-lookup"><span data-stu-id="79c3c-127">INPUTS</span></span>

## <span data-ttu-id="79c3c-128">출력</span><span class="sxs-lookup"><span data-stu-id="79c3c-128">OUTPUTS</span></span>

### <span data-ttu-id="79c3c-129">Api20200601. i p. p i p. IApiKey</span><span class="sxs-lookup"><span data-stu-id="79c3c-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="79c3c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="79c3c-130">NOTES</span></span>

<span data-ttu-id="79c3c-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="79c3c-131">ALIASES</span></span>

## <span data-ttu-id="79c3c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79c3c-132">RELATED LINKS</span></span>
