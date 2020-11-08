---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047691"
---
# <span data-ttu-id="37cf4-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="37cf4-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="37cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="37cf4-103">Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="37cf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37cf4-104">SYNTAX</span></span>

### <span data-ttu-id="37cf4-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="37cf4-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37cf4-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="37cf4-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37cf4-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="37cf4-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37cf4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37cf4-108">DESCRIPTION</span></span>
<span data-ttu-id="37cf4-109">**AzRecoveryServicesVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="37cf4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="37cf4-110">EXAMPLES</span></span>

### <span data-ttu-id="37cf4-111">예제 1: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="37cf4-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="37cf4-112">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="37cf4-113">두 번째 명령은 $CredsPath 변수를 C:\Downloads.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="37cf4-114">마지막 명령은 Azure 백업용 $CredsPath의 자격 증명을 사용 하 여 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="37cf4-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="37cf4-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="37cf4-116">명령이 자격 증명 모음 형식 siteRecovery의 01 $Vault에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="37cf4-117">예제 3: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="37cf4-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="37cf4-118">명령 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="37cf4-119">변수</span><span class="sxs-lookup"><span data-stu-id="37cf4-119">PARAMETERS</span></span>

### <span data-ttu-id="37cf4-120">-백업</span><span class="sxs-lookup"><span data-stu-id="37cf4-120">-Backup</span></span>
<span data-ttu-id="37cf4-121">자격 증명 모음 파일을 Azure 백업에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-122">-인증서</span><span class="sxs-lookup"><span data-stu-id="37cf4-122">-Certificate</span></span>
<span data-ttu-id="37cf4-123">{{인증서 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="37cf4-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="37cf4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cf4-124">-DefaultProfile</span></span>
<span data-ttu-id="37cf4-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37cf4-126">-Path</span><span class="sxs-lookup"><span data-stu-id="37cf4-126">-Path</span></span>
<span data-ttu-id="37cf4-127">Azure Site Recovery 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="37cf4-128">Azure Site Recovery 자격 증명 모음 포털에서이 파일을 다운로드 하 여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="37cf4-129">-SiteFriendlyName</span></span>
<span data-ttu-id="37cf4-130">사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="37cf4-131">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="37cf4-132">-SiteIdentifier</span></span>
<span data-ttu-id="37cf4-133">사이트 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-133">Specifies the site identifier.</span></span>
<span data-ttu-id="37cf4-134">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="37cf4-135">-SiteRecovery</span></span>
<span data-ttu-id="37cf4-136">자격 증명 모음 파일을 Azure Site Recovery에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-137">-저장실</span><span class="sxs-lookup"><span data-stu-id="37cf4-137">-Vault</span></span>
<span data-ttu-id="37cf4-138">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37cf4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cf4-139">CommonParameters</span></span>
<span data-ttu-id="37cf4-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cf4-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37cf4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cf4-142">입력</span><span class="sxs-lookup"><span data-stu-id="37cf4-142">INPUTS</span></span>

### <span data-ttu-id="37cf4-143">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="37cf4-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="37cf4-144">출력</span><span class="sxs-lookup"><span data-stu-id="37cf4-144">OUTPUTS</span></span>

### <span data-ttu-id="37cf4-145">VaultSettingsFilePath를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="37cf4-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="37cf4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="37cf4-146">NOTES</span></span>

## <span data-ttu-id="37cf4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37cf4-147">RELATED LINKS</span></span>

[<span data-ttu-id="37cf4-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="37cf4-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="37cf4-149">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="37cf4-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="37cf4-150">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="37cf4-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)

