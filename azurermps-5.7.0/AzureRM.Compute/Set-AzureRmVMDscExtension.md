---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529009"
---
# <span data-ttu-id="92ca9-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="92ca9-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="92ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="92ca9-103">가상 컴퓨터에서 DSC 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ca9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92ca9-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92ca9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="92ca9-106">**AzureRmVMDscExtension** cmdlet은 리소스 그룹의 가상 컴퓨터에서 Windows POWERSHELL의 DSC (원하는 상태 구성) 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="92ca9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="92ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="92ca9-108">예제 1: DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="92ca9-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="92ca9-109">이 명령은 VM07 이라는 가상 컴퓨터의 DSC 확장을 Stg 및 기본 컨테이너 라는 저장소 계정에서 Sample.ps1.zip 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="92ca9-110">명령에서 ConfigName 이라는 구성을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="92ca9-111">AzureRmVMDscConfiguration를 사용 하 여 이전에 업로드 **한** Sample.ps1.zip 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="92ca9-112">예제 2: 구성 데이터를 사용 하 여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="92ca9-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="92ca9-113">이 명령은 VM13 이라는 가상 컴퓨터의 확장명을 Stg와 WindowsPowerShellDSC 이라는 저장소 계정에서 Sample.ps1.zip를 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="92ca9-114">Command는 ConfigName 이라는 구성으로, 구성 데이터 및 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="92ca9-115">AzureRmVMDscConfiguration를 사용 하 여 이전에 업로드 **한** Sample.ps1.zip 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="92ca9-116">예제 3: 자동 업데이트가 있는 구성 데이터를 사용 하 여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="92ca9-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="92ca9-117">이 명령은 VM22 이라는 가상 컴퓨터의 확장명을 Stg와 WindowsPowerShellDSC 이라는 저장소 계정에서 Sample.ps1.zip를 다운로드 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="92ca9-118">명령에서 ConfigName 이라는 구성을 호출 하 고 구성 데이터 및 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="92ca9-119">또한이 명령을 사용 하면 확장 처리기를 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="92ca9-120">**AzureRmVMDscConfiguration** 를 사용 하 여 이전에 업로드 한 Sample.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="92ca9-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="92ca9-121">변수</span><span class="sxs-lookup"><span data-stu-id="92ca9-121">PARAMETERS</span></span>

### <span data-ttu-id="92ca9-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="92ca9-122">-ArchiveBlobName</span></span>
<span data-ttu-id="92ca9-123">이전에 Publish-AzureRmVMDscConfiguration cmdlet에 의해 업로드 된 구성 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="92ca9-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="92ca9-124">-ArchiveContainerName</span></span>
<span data-ttu-id="92ca9-125">구성 아카이브가 있는 Azure storage 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="92ca9-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ca9-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="92ca9-127">구성 보관 파일을 포함 하는 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="92ca9-128">저장소 계정 및 가상 컴퓨터가 모두 동일한 리소스 그룹에 있는 경우이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="92ca9-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="92ca9-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="92ca9-130">ArchiveBlobName를 다운로드 하는 데 사용 되는 Azure storage 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="92ca9-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="92ca9-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="92ca9-132">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="92ca9-133">-자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="92ca9-133">-AutoUpdate</span></span>
<span data-ttu-id="92ca9-134">*Version* 매개 변수에 의해 지정 된 확장 처리기 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="92ca9-135">기본적으로 확장 처리기는 autoupdated 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="92ca9-136">자동 업데이트 *매개 변수를 사용* 하 여 확장 처리기를 최신 버전과 함께 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="92ca9-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="92ca9-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="92ca9-137">-ConfigurationArgument</span></span>
<span data-ttu-id="92ca9-138">구성 함수에 대 한 인수를 포함 하는 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="92ca9-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="92ca9-139">-ConfigurationData</span></span>
<span data-ttu-id="92ca9-140">구성에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="92ca9-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="92ca9-141">-ConfigurationName</span></span>
<span data-ttu-id="92ca9-142">DSC 확장에서 호출 하는 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="92ca9-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="92ca9-143">-DataCollection</span></span>
<span data-ttu-id="92ca9-144">데이터 컬렉션 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-144">Specifies the data collection type.</span></span>
<span data-ttu-id="92ca9-145">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="92ca9-146">-Force</span><span class="sxs-lookup"><span data-stu-id="92ca9-146">-Force</span></span>
<span data-ttu-id="92ca9-147">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-147">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92ca9-148">-위치</span><span class="sxs-lookup"><span data-stu-id="92ca9-148">-Location</span></span>
<span data-ttu-id="92ca9-149">리소스 확장의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="92ca9-150">-이름</span><span class="sxs-lookup"><span data-stu-id="92ca9-150">-Name</span></span>
<span data-ttu-id="92ca9-151">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="92ca9-152">기본값은 Microsoft. i m m입니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="92ca9-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ca9-153">-ResourceGroupName</span></span>
<span data-ttu-id="92ca9-154">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-154">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="92ca9-155">-버전</span><span class="sxs-lookup"><span data-stu-id="92ca9-155">-Version</span></span>
<span data-ttu-id="92ca9-156">설정을 적용 Set-AzureRmVMDscExtension는 DSC 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="92ca9-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="92ca9-157">-VMName</span></span>
<span data-ttu-id="92ca9-158">DSC 확장 처리기가 설치 된 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="92ca9-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="92ca9-159">-WmfVersion</span></span>
<span data-ttu-id="92ca9-160">WMF 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-160">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="92ca9-161">-확인</span><span class="sxs-lookup"><span data-stu-id="92ca9-161">-Confirm</span></span>
<span data-ttu-id="92ca9-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ca9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ca9-163">-WhatIf</span></span>
<span data-ttu-id="92ca9-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="92ca9-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ca9-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ca9-166">CommonParameters</span></span>
<span data-ttu-id="92ca9-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ca9-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ca9-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ca9-169">입력</span><span class="sxs-lookup"><span data-stu-id="92ca9-169">INPUTS</span></span>

### <span data-ttu-id="92ca9-170">않아야</span><span class="sxs-lookup"><span data-stu-id="92ca9-170">None</span></span>
<span data-ttu-id="92ca9-171">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92ca9-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92ca9-172">출력</span><span class="sxs-lookup"><span data-stu-id="92ca9-172">OUTPUTS</span></span>

## <span data-ttu-id="92ca9-173">상속자</span><span class="sxs-lookup"><span data-stu-id="92ca9-173">NOTES</span></span>

## <span data-ttu-id="92ca9-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92ca9-174">RELATED LINKS</span></span>

[<span data-ttu-id="92ca9-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="92ca9-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="92ca9-176">제거-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="92ca9-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="92ca9-177">게시-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="92ca9-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)

