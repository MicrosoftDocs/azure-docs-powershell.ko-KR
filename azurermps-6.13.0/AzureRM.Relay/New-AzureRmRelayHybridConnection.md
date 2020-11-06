---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 1caf26a439cdc835d511ffb7bd6021dd5db1fa9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526091"
---
# <span data-ttu-id="13e6e-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="13e6e-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="13e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="13e6e-103">지정 된 릴레이 네임 스페이스에 HybridConnection를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13e6e-104">SYNTAX</span></span>

### <span data-ttu-id="13e6e-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13e6e-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13e6e-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="13e6e-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e6e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13e6e-107">DESCRIPTION</span></span>
<span data-ttu-id="13e6e-108">New-AzureRmRelayHybridConnection cmdlet은 지정 된 릴레이 네임 스페이스에 HybridConnection를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="13e6e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="13e6e-109">EXAMPLES</span></span>

### <span data-ttu-id="13e6e-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="13e6e-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="13e6e-111">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-HybirdConnection에 새 HybirdConnection TestHybirdConnection2를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="13e6e-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="13e6e-112">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="13e6e-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="13e6e-113">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-HybirdConnection에 새 HybirdConnection TestHybirdConnection1를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="13e6e-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="13e6e-114">변수</span><span class="sxs-lookup"><span data-stu-id="13e6e-114">PARAMETERS</span></span>

### <span data-ttu-id="13e6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e6e-115">-DefaultProfile</span></span>
<span data-ttu-id="13e6e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e6e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13e6e-117">-InputObject</span></span>
<span data-ttu-id="13e6e-118">HybridConnections 개체</span><span class="sxs-lookup"><span data-stu-id="13e6e-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e6e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="13e6e-119">-Name</span></span>
<span data-ttu-id="13e6e-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e6e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13e6e-121">-Namespace</span></span>
<span data-ttu-id="13e6e-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-122">Namespace Name.</span></span>

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

### <span data-ttu-id="13e6e-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="13e6e-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="13e6e-124">이 HybridConnections에 대해 클라이언트 인증이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="13e6e-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="13e6e-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="13e6e-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="13e6e-127">-UserMetadata</span></span>
<span data-ttu-id="13e6e-128">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e6e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="13e6e-129">-Confirm</span></span>
<span data-ttu-id="13e6e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e6e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e6e-131">-WhatIf</span></span>
<span data-ttu-id="13e6e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13e6e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e6e-134">CommonParameters</span></span>
<span data-ttu-id="13e6e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="13e6e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e6e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e6e-137">입력</span><span class="sxs-lookup"><span data-stu-id="13e6e-137">INPUTS</span></span>

### <span data-ttu-id="13e6e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13e6e-138">System.String</span></span>
<span data-ttu-id="13e6e-139">PSHybridConnectionAttibutes System. Null 허용 ' 1 [[4.0.0.0], [시스템 부울, mscorlib, Version =, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="13e6e-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="13e6e-140">출력</span><span class="sxs-lookup"><span data-stu-id="13e6e-140">OUTPUTS</span></span>

### <span data-ttu-id="13e6e-141">PSHybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="13e6e-141">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="13e6e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="13e6e-142">NOTES</span></span>

## <span data-ttu-id="13e6e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13e6e-143">RELATED LINKS</span></span>