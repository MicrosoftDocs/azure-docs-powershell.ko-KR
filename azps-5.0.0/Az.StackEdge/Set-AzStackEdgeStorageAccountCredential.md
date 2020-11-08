---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217198"
---
# <span data-ttu-id="208f3-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="208f3-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="208f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="208f3-102">SYNOPSIS</span></span>
<span data-ttu-id="208f3-103">장치에 대 한 저장소 계정 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="208f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="208f3-104">SYNTAX</span></span>

### <span data-ttu-id="208f3-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="208f3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208f3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="208f3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="208f3-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="208f3-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208f3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="208f3-108">DESCRIPTION</span></span>
<span data-ttu-id="208f3-109">**AzStackEdgeStorageAccountCredential** Cmdlet은 스택 경계 디바이스의 저장소 계정에 해당 하는 저장소 계정 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="208f3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="208f3-110">EXAMPLES</span></span>

### <span data-ttu-id="208f3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="208f3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="208f3-112">저장소 계정의 선택 키 회전에 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="208f3-113">변수</span><span class="sxs-lookup"><span data-stu-id="208f3-113">PARAMETERS</span></span>

### <span data-ttu-id="208f3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="208f3-114">-AsJob</span></span>
<span data-ttu-id="208f3-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="208f3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="208f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208f3-116">-DefaultProfile</span></span>
<span data-ttu-id="208f3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="208f3-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="208f3-118">-DeviceName</span></span>
<span data-ttu-id="208f3-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="208f3-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-120">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="208f3-120">-EncryptionKey</span></span>
<span data-ttu-id="208f3-121">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="208f3-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="208f3-122">-InputObject</span></span>
<span data-ttu-id="208f3-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="208f3-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="208f3-124">-Name</span></span>
<span data-ttu-id="208f3-125">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="208f3-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="208f3-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="208f3-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="208f3-128">-ResourceId</span></span>
<span data-ttu-id="208f3-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="208f3-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="208f3-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="208f3-131">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="208f3-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208f3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="208f3-132">-Confirm</span></span>
<span data-ttu-id="208f3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208f3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208f3-134">-WhatIf</span></span>
<span data-ttu-id="208f3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="208f3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208f3-137">CommonParameters</span></span>
<span data-ttu-id="208f3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="208f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208f3-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="208f3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208f3-140">입력</span><span class="sxs-lookup"><span data-stu-id="208f3-140">INPUTS</span></span>

### <span data-ttu-id="208f3-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="208f3-141">System.String</span></span>

### <span data-ttu-id="208f3-142">StackEdge. PSStackEdgeStorageAccountCredential에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="208f3-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="208f3-143">출력</span><span class="sxs-lookup"><span data-stu-id="208f3-143">OUTPUTS</span></span>

### <span data-ttu-id="208f3-144">StackEdge. PSStackEdgeStorageAccountCredential에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="208f3-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="208f3-145">상속자</span><span class="sxs-lookup"><span data-stu-id="208f3-145">NOTES</span></span>

## <span data-ttu-id="208f3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="208f3-146">RELATED LINKS</span></span>