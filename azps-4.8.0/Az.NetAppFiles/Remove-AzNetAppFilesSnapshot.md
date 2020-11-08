---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048167"
---
# <span data-ttu-id="16b44-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="16b44-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="16b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b44-102">SYNOPSIS</span></span>
<span data-ttu-id="16b44-103">ANF (Azure NetApp Files) 스냅숏을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="16b44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16b44-104">SYNTAX</span></span>

### <span data-ttu-id="16b44-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="16b44-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b44-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16b44-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b44-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16b44-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b44-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16b44-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b44-109">설명은</span><span class="sxs-lookup"><span data-stu-id="16b44-109">DESCRIPTION</span></span>
<span data-ttu-id="16b44-110">**AzNetAppFilesSnapshot** cmdlet은 anf 스냅숏을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="16b44-111">예제의</span><span class="sxs-lookup"><span data-stu-id="16b44-111">EXAMPLES</span></span>

### <span data-ttu-id="16b44-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="16b44-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="16b44-113">이 명령은 ANF 스냅숏 "MyAnfSnapshot"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="16b44-114">변수</span><span class="sxs-lookup"><span data-stu-id="16b44-114">PARAMETERS</span></span>

### <span data-ttu-id="16b44-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16b44-115">-AccountName</span></span>
<span data-ttu-id="16b44-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="16b44-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="16b44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b44-117">-DefaultProfile</span></span>
<span data-ttu-id="16b44-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16b44-119">-InputObject</span></span>
<span data-ttu-id="16b44-120">제거할 스냅숏 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16b44-121">-이름</span><span class="sxs-lookup"><span data-stu-id="16b44-121">-Name</span></span>
<span data-ttu-id="16b44-122">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="16b44-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b44-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16b44-123">-PassThru</span></span>
<span data-ttu-id="16b44-124">지정 된 볼륨이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="16b44-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="16b44-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="16b44-125">-PoolName</span></span>
<span data-ttu-id="16b44-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="16b44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b44-127">-ResourceGroupName</span></span>
<span data-ttu-id="16b44-128">ANF 스냅숏의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="16b44-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="16b44-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16b44-129">-ResourceId</span></span>
<span data-ttu-id="16b44-130">ANF 스냅숏의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="16b44-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="16b44-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="16b44-131">-VolumeName</span></span>
<span data-ttu-id="16b44-132">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="16b44-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="16b44-133">-VolumeObject</span></span>
<span data-ttu-id="16b44-134">제거할 스냅숏이 포함 된 volume 개체</span><span class="sxs-lookup"><span data-stu-id="16b44-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16b44-135">-확인</span><span class="sxs-lookup"><span data-stu-id="16b44-135">-Confirm</span></span>
<span data-ttu-id="16b44-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b44-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b44-137">-WhatIf</span></span>
<span data-ttu-id="16b44-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b44-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b44-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b44-140">CommonParameters</span></span>
<span data-ttu-id="16b44-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b44-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b44-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16b44-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b44-143">입력</span><span class="sxs-lookup"><span data-stu-id="16b44-143">INPUTS</span></span>

### <span data-ttu-id="16b44-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16b44-144">System.String</span></span>

### <span data-ttu-id="16b44-145">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="16b44-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="16b44-146">PSNetAppFilesSnapshot-. p m.</span><span class="sxs-lookup"><span data-stu-id="16b44-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="16b44-147">출력</span><span class="sxs-lookup"><span data-stu-id="16b44-147">OUTPUTS</span></span>

### <span data-ttu-id="16b44-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="16b44-148">System.Boolean</span></span>

## <span data-ttu-id="16b44-149">상속자</span><span class="sxs-lookup"><span data-stu-id="16b44-149">NOTES</span></span>

## <span data-ttu-id="16b44-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16b44-150">RELATED LINKS</span></span>