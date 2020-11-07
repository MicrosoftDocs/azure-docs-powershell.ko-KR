---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: ccad3d793ec5763a4c7db44d2b5ff3583b35402b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876867"
---
# <span data-ttu-id="9df3d-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9df3d-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="9df3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df3d-102">SYNOPSIS</span></span>
<span data-ttu-id="9df3d-103">가상 컴퓨터에서 DSC 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="9df3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9df3d-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9df3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9df3d-105">DESCRIPTION</span></span>
<span data-ttu-id="9df3d-106">**AzVMDscExtension** cmdlet은 리소스 그룹의 가상 컴퓨터에서 Windows POWERSHELL의 DSC (원하는 상태 구성) 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="9df3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9df3d-107">EXAMPLES</span></span>

### <span data-ttu-id="9df3d-108">예제 1: DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="9df3d-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="9df3d-109">이 명령은 VM07 이라는 가상 컴퓨터의 DSC 확장을 Stg 및 기본 컨테이너 라는 저장소 계정에서 Sample.ps1.zip 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="9df3d-110">명령에서 ConfigName 이라는 구성을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="9df3d-111">AzVMDscConfiguration를 사용 하 여 이전에 업로드 **한** Sample.ps1.zip 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="9df3d-112">예제 2: 구성 데이터를 사용 하 여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="9df3d-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="9df3d-113">이 명령은 VM13 이라는 가상 컴퓨터의 확장명을 Stg와 WindowsPowerShellDSC 이라는 저장소 계정에서 Sample.ps1.zip를 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="9df3d-114">Command는 ConfigName 이라는 구성으로, 구성 데이터 및 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="9df3d-115">AzVMDscConfiguration를 사용 하 여 이전에 업로드 **한** Sample.ps1.zip 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="9df3d-116">예제 3: 자동 업데이트가 있는 구성 데이터를 사용 하 여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="9df3d-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="9df3d-117">이 명령은 VM22 이라는 가상 컴퓨터의 확장명을 Stg와 WindowsPowerShellDSC 이라는 저장소 계정에서 Sample.ps1.zip를 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="9df3d-118">명령에서 ConfigName 이라는 구성을 호출 하 고 구성 데이터 및 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="9df3d-119">또한이 명령을 사용 하면 확장 처리기를 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="9df3d-120">**AzVMDscConfiguration** 를 사용 하 여 이전에 업로드 한 Sample.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="9df3d-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="9df3d-121">변수</span><span class="sxs-lookup"><span data-stu-id="9df3d-121">PARAMETERS</span></span>

### <span data-ttu-id="9df3d-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="9df3d-122">-ArchiveBlobName</span></span>
<span data-ttu-id="9df3d-123">이전에 Publish-AzVMDscConfiguration cmdlet에 의해 업로드 된 구성 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="9df3d-124">-ArchiveContainerName</span></span>
<span data-ttu-id="9df3d-125">구성 아카이브가 있는 Azure storage 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df3d-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="9df3d-127">구성 보관 파일을 포함 하는 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="9df3d-128">저장소 계정 및 가상 컴퓨터가 모두 동일한 리소스 그룹에 있는 경우이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9df3d-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="9df3d-130">ArchiveBlobName를 다운로드 하는 데 사용 되는 Azure storage 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9df3d-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="9df3d-132">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-133">-자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="9df3d-133">-AutoUpdate</span></span>
<span data-ttu-id="9df3d-134">*Version* 매개 변수에 의해 지정 된 확장 처리기 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="9df3d-135">기본적으로 확장 처리기는 autoupdated 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="9df3d-136">자동 업데이트 *매개 변수를 사용* 하 여 확장 처리기를 최신 버전과 함께 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="9df3d-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="9df3d-137">-ConfigurationArgument</span></span>
<span data-ttu-id="9df3d-138">구성 함수에 대 한 인수를 포함 하는 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="9df3d-139">-ConfigurationData</span></span>
<span data-ttu-id="9df3d-140">구성에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9df3d-141">-ConfigurationName</span></span>
<span data-ttu-id="9df3d-142">DSC 확장에서 호출 하는 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="9df3d-143">-DataCollection</span></span>
<span data-ttu-id="9df3d-144">데이터 컬렉션 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-144">Specifies the data collection type.</span></span>
<span data-ttu-id="9df3d-145">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df3d-146">-DefaultProfile</span></span>
<span data-ttu-id="9df3d-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-148">-Force</span><span class="sxs-lookup"><span data-stu-id="9df3d-148">-Force</span></span>
<span data-ttu-id="9df3d-149">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-149">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-150">-위치</span><span class="sxs-lookup"><span data-stu-id="9df3d-150">-Location</span></span>
<span data-ttu-id="9df3d-151">리소스 확장의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-152">-이름</span><span class="sxs-lookup"><span data-stu-id="9df3d-152">-Name</span></span>
<span data-ttu-id="9df3d-153">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9df3d-154">기본값은 Microsoft. i m m입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df3d-155">-ResourceGroupName</span></span>
<span data-ttu-id="9df3d-156">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-156">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-157">-버전</span><span class="sxs-lookup"><span data-stu-id="9df3d-157">-Version</span></span>
<span data-ttu-id="9df3d-158">설정을 적용 Set-AzVMDscExtension는 DSC 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="9df3d-159">-VMName</span></span>
<span data-ttu-id="9df3d-160">DSC 확장 처리기가 설치 된 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="9df3d-161">-WmfVersion</span></span>
<span data-ttu-id="9df3d-162">WMF 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-162">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-163">-확인</span><span class="sxs-lookup"><span data-stu-id="9df3d-163">-Confirm</span></span>
<span data-ttu-id="9df3d-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9df3d-165">-WhatIf</span></span>
<span data-ttu-id="9df3d-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-166">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9df3d-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df3d-168">CommonParameters</span></span>
<span data-ttu-id="9df3d-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df3d-170">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df3d-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df3d-171">입력</span><span class="sxs-lookup"><span data-stu-id="9df3d-171">INPUTS</span></span>

### <span data-ttu-id="9df3d-172">않아야</span><span class="sxs-lookup"><span data-stu-id="9df3d-172">None</span></span>
<span data-ttu-id="9df3d-173">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9df3d-174">출력</span><span class="sxs-lookup"><span data-stu-id="9df3d-174">OUTPUTS</span></span>

### <span data-ttu-id="9df3d-175">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9df3d-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9df3d-176">상속자</span><span class="sxs-lookup"><span data-stu-id="9df3d-176">NOTES</span></span>

## <span data-ttu-id="9df3d-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9df3d-177">RELATED LINKS</span></span>

[<span data-ttu-id="9df3d-178">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9df3d-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="9df3d-179">제거-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9df3d-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="9df3d-180">게시-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9df3d-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)

