---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525364"
---
# <span data-ttu-id="609a4-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="609a4-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="609a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609a4-102">SYNOPSIS</span></span>
<span data-ttu-id="609a4-103">자동화 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="609a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="609a4-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609a4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="609a4-105">DESCRIPTION</span></span>
<span data-ttu-id="609a4-106">**AzureRmAutomationCertificate** Cmdlet은 Azure Automation에서 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="609a4-107">업로드할 인증서 파일의 경로를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="609a4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="609a4-108">EXAMPLES</span></span>

### <span data-ttu-id="609a4-109">예제 1: 새 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="609a4-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="609a4-110">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 안전한 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="609a4-111">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="609a4-112">두 번째 명령은 ContosoCertificate 이라는 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="609a4-113">이 명령은 $Password에 저장 된 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="609a4-114">명령은 계정 이름과 업로드 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="609a4-115">변수</span><span class="sxs-lookup"><span data-stu-id="609a4-115">PARAMETERS</span></span>

### <span data-ttu-id="609a4-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="609a4-116">-AutomationAccountName</span></span>
<span data-ttu-id="609a4-117">이 cmdlet이 인증서를 저장 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609a4-118">-DefaultProfile</span></span>
<span data-ttu-id="609a4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="609a4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="609a4-120">-설명</span><span class="sxs-lookup"><span data-stu-id="609a4-120">-Description</span></span>
<span data-ttu-id="609a4-121">인증서에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="609a4-122">-내보내기 가능한</span><span class="sxs-lookup"><span data-stu-id="609a4-122">-Exportable</span></span>
<span data-ttu-id="609a4-123">인증서를 내보낼 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609a4-124">-이름</span><span class="sxs-lookup"><span data-stu-id="609a4-124">-Name</span></span>
<span data-ttu-id="609a4-125">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="609a4-126">-암호</span><span class="sxs-lookup"><span data-stu-id="609a4-126">-Password</span></span>
<span data-ttu-id="609a4-127">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609a4-128">-Path</span><span class="sxs-lookup"><span data-stu-id="609a4-128">-Path</span></span>
<span data-ttu-id="609a4-129">이 cmdlet이 업로드 하는 스크립트 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="609a4-130">파일은 .cer 또는 .pfx 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="609a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="609a4-132">이 cmdlet이 인증서를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609a4-133">CommonParameters</span></span>
<span data-ttu-id="609a4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609a4-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="609a4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609a4-136">입력</span><span class="sxs-lookup"><span data-stu-id="609a4-136">INPUTS</span></span>

### <span data-ttu-id="609a4-137">않아야</span><span class="sxs-lookup"><span data-stu-id="609a4-137">None</span></span>
<span data-ttu-id="609a4-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="609a4-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="609a4-139">출력</span><span class="sxs-lookup"><span data-stu-id="609a4-139">OUTPUTS</span></span>

### <span data-ttu-id="609a4-140">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="609a4-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="609a4-141">상속자</span><span class="sxs-lookup"><span data-stu-id="609a4-141">NOTES</span></span>

## <span data-ttu-id="609a4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="609a4-142">RELATED LINKS</span></span>

[<span data-ttu-id="609a4-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="609a4-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="609a4-144">제거-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="609a4-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="609a4-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="609a4-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)

