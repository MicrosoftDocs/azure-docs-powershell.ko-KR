---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: e3e4858e3cb4f3c54c502ac14fb2c5d8e3ba0c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524604"
---
# <span data-ttu-id="5eebf-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5eebf-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="5eebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eebf-102">SYNOPSIS</span></span>
<span data-ttu-id="5eebf-103">백업 자격 증명 모음에 대 한 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eebf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5eebf-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eebf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5eebf-105">DESCRIPTION</span></span>
<span data-ttu-id="5eebf-106">**AzureRmBackupProtectionPolicy** Cmdlet은 Azure backup 자격 증명 모음에 대 한 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="5eebf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5eebf-107">EXAMPLES</span></span>

### <span data-ttu-id="5eebf-108">예제 1: 자격 증명 모음의 정책 보기</span><span class="sxs-lookup"><span data-stu-id="5eebf-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="5eebf-109">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="5eebf-110">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-110">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="5eebf-111">두 번째 명령은 $Vault의 자격 증명 모음에 대 한 모든 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="5eebf-112">예제 2: 자격 증명 모음에서 특정 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="5eebf-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="5eebf-113">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="5eebf-114">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-114">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="5eebf-115">두 번째 명령은 $Vault의 자격 증명 모음에 대 한 DefaultPolicy 라는 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="5eebf-116">변수</span><span class="sxs-lookup"><span data-stu-id="5eebf-116">PARAMETERS</span></span>

### <span data-ttu-id="5eebf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eebf-117">-DefaultProfile</span></span>
<span data-ttu-id="5eebf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5eebf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eebf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5eebf-119">-Name</span></span>
<span data-ttu-id="5eebf-120">이 cmdlet이 가져오는 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-120">Specifies the name of the policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eebf-121">-저장실</span><span class="sxs-lookup"><span data-stu-id="5eebf-121">-Vault</span></span>
<span data-ttu-id="5eebf-122">이 cmdlet에서 정책을 가져오는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="5eebf-123">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eebf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eebf-124">CommonParameters</span></span>
<span data-ttu-id="5eebf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eebf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eebf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eebf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eebf-127">입력</span><span class="sxs-lookup"><span data-stu-id="5eebf-127">INPUTS</span></span>

### <span data-ttu-id="5eebf-128">AzureRMBackupVault를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="5eebf-128">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="5eebf-129">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5eebf-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="5eebf-130">출력</span><span class="sxs-lookup"><span data-stu-id="5eebf-130">OUTPUTS</span></span>

### <span data-ttu-id="5eebf-131">AzureRMBackupProtectionPolicy를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="5eebf-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="5eebf-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5eebf-132">NOTES</span></span>

## <span data-ttu-id="5eebf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5eebf-133">RELATED LINKS</span></span>

[<span data-ttu-id="5eebf-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5eebf-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="5eebf-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5eebf-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="5eebf-136">새로운 AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5eebf-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="5eebf-137">제거-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5eebf-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

