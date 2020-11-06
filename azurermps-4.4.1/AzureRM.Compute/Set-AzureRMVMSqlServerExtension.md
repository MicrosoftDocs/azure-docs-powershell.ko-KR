---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a89a2fc342bf1a3ed6e311057f55bb83c80be210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528243"
---
# <span data-ttu-id="d719e-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d719e-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="d719e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d719e-102">SYNOPSIS</span></span>
<span data-ttu-id="d719e-103">가상 컴퓨터에서 Azure SQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d719e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d719e-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d719e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d719e-105">DESCRIPTION</span></span>
<span data-ttu-id="d719e-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 컴퓨터의 AzureSQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="d719e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d719e-107">EXAMPLES</span></span>

### <span data-ttu-id="d719e-108">예제 1: 가상 컴퓨터에서 자동 패치 설정 설정</span><span class="sxs-lookup"><span data-stu-id="d719e-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="d719e-109">첫 번째 명령은 **New AzureVMSqlServerAutoPatchingConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="d719e-110">명령은 $AutoPatchingConfig 변수에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="d719e-111">두 번째 명령은 Get-AzureRmVM cmdlet을 사용 하 여 Service02 이라는 서비스에서 VirtualMachine11 라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="d719e-112">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="d719e-113">현재 cmdlet은 가상 컴퓨터에 대 한 $AutoPatchingConfig에서 자동 패치 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="d719e-114">명령이 가상 컴퓨터를 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="d719e-115">예제 2: 가상 컴퓨터에서 자동 백업 설정 설정</span><span class="sxs-lookup"><span data-stu-id="d719e-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="d719e-116">첫 번째 명령은 **New AzureVMSqlServerAutoBackupConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="d719e-117">명령은 $AutoBackupConfig 변수에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="d719e-118">두 번째 명령은 Service02 이라는 서비스에서 VirtualMachine11 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="d719e-119">현재 cmdlet은 가상 컴퓨터에 대 한 $AutoBackupConfig에서 자동 백업 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="d719e-120">명령이 가상 컴퓨터를 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="d719e-121">예제 3: 가상 컴퓨터에서 SQL Server 확장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d719e-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="d719e-122">이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d719e-123">이 명령은 해당 가상 컴퓨터에서 SQL Server 가상 컴퓨터 확장을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="d719e-124">예제 4: 특정 가상 컴퓨터에서 SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="d719e-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="d719e-125">이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d719e-126">명령에서 해당 가상 컴퓨터의 SQL Server 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="d719e-127">변수</span><span class="sxs-lookup"><span data-stu-id="d719e-127">PARAMETERS</span></span>

### <span data-ttu-id="d719e-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d719e-128">-AutoBackupSettings</span></span>
<span data-ttu-id="d719e-129">SQL Server 자동 백업 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="d719e-130">**AutoBackupSettings** 개체를 만들려면 New-AzureVMSqlServerAutoBackupConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d719e-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="d719e-132">SQL Server 자동 패치 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="d719e-133">**AutoPatchingSettings** 개체를 만들려면 New-AzureVMSqlServerAutoPatchingConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d719e-134">-DefaultProfile</span></span>
<span data-ttu-id="d719e-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d719e-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d719e-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-137">-위치</span><span class="sxs-lookup"><span data-stu-id="d719e-137">-Location</span></span>
<span data-ttu-id="d719e-138">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-139">-이름</span><span class="sxs-lookup"><span data-stu-id="d719e-139">-Name</span></span>
<span data-ttu-id="d719e-140">확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d719e-141">-ResourceGroupName</span></span>
<span data-ttu-id="d719e-142">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d719e-143">-버전</span><span class="sxs-lookup"><span data-stu-id="d719e-143">-Version</span></span>
<span data-ttu-id="d719e-144">SQL Server 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d719e-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="d719e-145">-VMName</span></span>
<span data-ttu-id="d719e-146">이 cmdlet에서 SQL Server 확장을 설정 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="d719e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d719e-147">CommonParameters</span></span>
<span data-ttu-id="d719e-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d719e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d719e-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d719e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d719e-150">입력</span><span class="sxs-lookup"><span data-stu-id="d719e-150">INPUTS</span></span>

## <span data-ttu-id="d719e-151">출력</span><span class="sxs-lookup"><span data-stu-id="d719e-151">OUTPUTS</span></span>

## <span data-ttu-id="d719e-152">상속자</span><span class="sxs-lookup"><span data-stu-id="d719e-152">NOTES</span></span>

## <span data-ttu-id="d719e-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d719e-153">RELATED LINKS</span></span>

[<span data-ttu-id="d719e-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d719e-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d719e-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d719e-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="d719e-156">새로운 AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d719e-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="d719e-157">새로운 AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d719e-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="d719e-158">제거-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d719e-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="d719e-159">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d719e-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

