---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: f26f21e197653c11b06a57fb5cb01a46ae808003
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873423"
---
# <span data-ttu-id="548b6-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="548b6-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="548b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548b6-102">SYNOPSIS</span></span>
<span data-ttu-id="548b6-103">지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="548b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="548b6-104">SYNTAX</span></span>

### <span data-ttu-id="548b6-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="548b6-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="548b6-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="548b6-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548b6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="548b6-107">DESCRIPTION</span></span>
<span data-ttu-id="548b6-108">Set-AzRelayHybridConnection cmdlet은 지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="548b6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="548b6-109">EXAMPLES</span></span>

### <span data-ttu-id="548b6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="548b6-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="548b6-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="548b6-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="548b6-112">지정 된 HybridConnection를 지정 된 네임 스페이스의 새 설명으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="548b6-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="548b6-114">변수</span><span class="sxs-lookup"><span data-stu-id="548b6-114">PARAMETERS</span></span>

### <span data-ttu-id="548b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548b6-115">-DefaultProfile</span></span>
<span data-ttu-id="548b6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="548b6-117">-InputObject</span></span>
<span data-ttu-id="548b6-118">HybridConnections 개체</span><span class="sxs-lookup"><span data-stu-id="548b6-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="548b6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="548b6-119">-Name</span></span>
<span data-ttu-id="548b6-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="548b6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="548b6-121">-Namespace</span></span>
<span data-ttu-id="548b6-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-122">Namespace Name.</span></span>

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

### <span data-ttu-id="548b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="548b6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="548b6-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="548b6-125">-UserMetadata</span></span>
<span data-ttu-id="548b6-126">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="548b6-127">-확인</span><span class="sxs-lookup"><span data-stu-id="548b6-127">-Confirm</span></span>
<span data-ttu-id="548b6-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548b6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548b6-129">-WhatIf</span></span>
<span data-ttu-id="548b6-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548b6-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548b6-132">CommonParameters</span></span>
<span data-ttu-id="548b6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="548b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548b6-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548b6-135">입력</span><span class="sxs-lookup"><span data-stu-id="548b6-135">INPUTS</span></span>

### <span data-ttu-id="548b6-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="548b6-136">System.String</span></span>

### <span data-ttu-id="548b6-137">PSHybridConnectionAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="548b6-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="548b6-138">출력</span><span class="sxs-lookup"><span data-stu-id="548b6-138">OUTPUTS</span></span>

### <span data-ttu-id="548b6-139">PSHybridConnectionAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="548b6-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="548b6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="548b6-140">NOTES</span></span>

## <span data-ttu-id="548b6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="548b6-141">RELATED LINKS</span></span>