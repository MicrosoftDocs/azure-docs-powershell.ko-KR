---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323455"
---
# <span data-ttu-id="940e2-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="940e2-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="940e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="940e2-102">SYNOPSIS</span></span>
<span data-ttu-id="940e2-103">SignalR 서비스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="940e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="940e2-104">SYNTAX</span></span>

### <span data-ttu-id="940e2-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="940e2-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="940e2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="940e2-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="940e2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="940e2-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="940e2-108">설명</span><span class="sxs-lookup"><span data-stu-id="940e2-108">DESCRIPTION</span></span>
<span data-ttu-id="940e2-109">SignalR 서비스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="940e2-110">예제</span><span class="sxs-lookup"><span data-stu-id="940e2-110">EXAMPLES</span></span>

### <span data-ttu-id="940e2-111">특정 SignalR 서비스의 액세스 키 얻기</span><span class="sxs-lookup"><span data-stu-id="940e2-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="940e2-112">파이프의 SignalR service 개체에서 선택키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="940e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="940e2-113">PARAMETERS</span></span>

### <span data-ttu-id="940e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940e2-114">-DefaultProfile</span></span>
<span data-ttu-id="940e2-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="940e2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="940e2-116">-InputObject</span></span>
<span data-ttu-id="940e2-117">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="940e2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="940e2-118">-Name</span></span>
<span data-ttu-id="940e2-119">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="940e2-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940e2-122">-ResourceId</span></span>
<span data-ttu-id="940e2-123">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="940e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940e2-124">CommonParameters</span></span>
<span data-ttu-id="940e2-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="940e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940e2-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="940e2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940e2-127">입력</span><span class="sxs-lookup"><span data-stu-id="940e2-127">INPUTS</span></span>

### <span data-ttu-id="940e2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="940e2-128">System.String</span></span>
### <span data-ttu-id="940e2-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="940e2-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="940e2-130">출력</span><span class="sxs-lookup"><span data-stu-id="940e2-130">OUTPUTS</span></span>

### <span data-ttu-id="940e2-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="940e2-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="940e2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="940e2-132">NOTES</span></span>

## <span data-ttu-id="940e2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="940e2-133">RELATED LINKS</span></span>