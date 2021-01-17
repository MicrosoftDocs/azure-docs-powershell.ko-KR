---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381893"
---
# <span data-ttu-id="486cd-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="486cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="486cd-102">SYNOPSIS</span></span>
<span data-ttu-id="486cd-103">지정된 Azure Storage Blob에서 API Management 서비스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="486cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="486cd-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="486cd-105">설명</span><span class="sxs-lookup"><span data-stu-id="486cd-105">DESCRIPTION</span></span>
<span data-ttu-id="486cd-106">**Restore-AzApiManagement** cmdlet은 Azurestorage Blob에 있는 지정된 백업에서 API Management 서비스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="486cd-107">예제</span><span class="sxs-lookup"><span data-stu-id="486cd-107">EXAMPLES</span></span>

### <span data-ttu-id="486cd-108">예제 1: API Management 서비스 복원</span><span class="sxs-lookup"><span data-stu-id="486cd-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="486cd-109">이 명령은 Azure Storage Blob에서 API Management 서비스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="486cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="486cd-110">PARAMETERS</span></span>

### <span data-ttu-id="486cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486cd-111">-DefaultProfile</span></span>
<span data-ttu-id="486cd-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="486cd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="486cd-113">-Name</span></span>
<span data-ttu-id="486cd-114">백업을 통해 복원할 API Management 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486cd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="486cd-115">-PassThru</span></span>
<span data-ttu-id="486cd-116">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="486cd-117">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="486cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="486cd-119">API Management가 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486cd-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="486cd-120">-SourceBlobName</span></span>
<span data-ttu-id="486cd-121">Azure 저장소 백업 원본 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486cd-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="486cd-122">-SourceContainerName</span></span>
<span data-ttu-id="486cd-123">Azure 저장소 백업 원본 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486cd-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="486cd-124">-StorageContext</span></span>
<span data-ttu-id="486cd-125">저장소 연결 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486cd-126">CommonParameters</span></span>
<span data-ttu-id="486cd-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="486cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486cd-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="486cd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486cd-129">입력</span><span class="sxs-lookup"><span data-stu-id="486cd-129">INPUTS</span></span>

### <span data-ttu-id="486cd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="486cd-130">System.String</span></span>

## <span data-ttu-id="486cd-131">출력</span><span class="sxs-lookup"><span data-stu-id="486cd-131">OUTPUTS</span></span>

### <span data-ttu-id="486cd-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="486cd-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="486cd-133">NOTES</span></span>

## <span data-ttu-id="486cd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="486cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="486cd-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="486cd-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="486cd-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="486cd-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="486cd-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

