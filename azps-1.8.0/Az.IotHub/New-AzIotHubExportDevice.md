---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 72c0793f75e00ec46a27cda476163f7cc0c93090
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868090"
---
# <span data-ttu-id="c850a-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="c850a-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="c850a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c850a-102">SYNOPSIS</span></span>
<span data-ttu-id="c850a-103">새 장치 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="c850a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c850a-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c850a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c850a-105">DESCRIPTION</span></span>
<span data-ttu-id="c850a-106">IotHub에 대 한 새 기기 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="c850a-107">이렇게 하면 모든 장치가 지정 된 컨테이너로 내보내기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="c850a-108">SAS URI를 생성 하는 방법에 대해서는 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c850a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="c850a-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="c850a-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="c850a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c850a-110">EXAMPLES</span></span>

### <span data-ttu-id="c850a-111">예제 1에서는 내보내기 장치 요청을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="c850a-112">키를 제외 하 고 IotHub "myiothub"에 대 한 새 내보내기 장치 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="c850a-113">변수</span><span class="sxs-lookup"><span data-stu-id="c850a-113">PARAMETERS</span></span>

### <span data-ttu-id="c850a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c850a-114">-DefaultProfile</span></span>
<span data-ttu-id="c850a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c850a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c850a-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="c850a-116">-ExcludeKeys</span></span>
<span data-ttu-id="c850a-117">키가 없는 장치를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="c850a-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="c850a-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="c850a-119">Blob을 내보낼 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="c850a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c850a-120">-Name</span></span>
<span data-ttu-id="c850a-121">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="c850a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c850a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c850a-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c850a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c850a-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c850a-124">-Confirm</span></span>
<span data-ttu-id="c850a-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c850a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c850a-126">-WhatIf</span></span>
<span data-ttu-id="c850a-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c850a-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c850a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c850a-129">CommonParameters</span></span>
<span data-ttu-id="c850a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c850a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c850a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c850a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c850a-132">입력</span><span class="sxs-lookup"><span data-stu-id="c850a-132">INPUTS</span></span>

### <span data-ttu-id="c850a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c850a-133">System.String</span></span>

## <span data-ttu-id="c850a-134">출력</span><span class="sxs-lookup"><span data-stu-id="c850a-134">OUTPUTS</span></span>

### <span data-ttu-id="c850a-135">IotHub. PSIotHubJobResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="c850a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="c850a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c850a-136">NOTES</span></span>

## <span data-ttu-id="c850a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c850a-137">RELATED LINKS</span></span>