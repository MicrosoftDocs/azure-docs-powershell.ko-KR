---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226441"
---
# <span data-ttu-id="be1b9-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="be1b9-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="be1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="be1b9-103">지정 된 Azure storage blob에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="be1b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be1b9-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be1b9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="be1b9-106">**AzApiManagement** Cmdlet은 azurestorage blob에 상주 하는 지정 된 백업에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="be1b9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="be1b9-108">예제 1: API Management 서비스 복원</span><span class="sxs-lookup"><span data-stu-id="be1b9-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="be1b9-109">이 명령은 Azure storage blob에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="be1b9-110">변수</span><span class="sxs-lookup"><span data-stu-id="be1b9-110">PARAMETERS</span></span>

### <span data-ttu-id="be1b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1b9-111">-DefaultProfile</span></span>
<span data-ttu-id="be1b9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be1b9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="be1b9-113">-Name</span></span>
<span data-ttu-id="be1b9-114">백업과 함께 복원 될 API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="be1b9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be1b9-115">-PassThru</span></span>
<span data-ttu-id="be1b9-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be1b9-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be1b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be1b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="be1b9-119">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="be1b9-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="be1b9-120">-SourceBlobName</span></span>
<span data-ttu-id="be1b9-121">Azure 저장소 백업 원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="be1b9-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="be1b9-122">-SourceContainerName</span></span>
<span data-ttu-id="be1b9-123">Azure 저장소 백업 원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="be1b9-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="be1b9-124">-StorageContext</span></span>
<span data-ttu-id="be1b9-125">저장소 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="be1b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1b9-126">CommonParameters</span></span>
<span data-ttu-id="be1b9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be1b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1b9-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be1b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1b9-129">입력</span><span class="sxs-lookup"><span data-stu-id="be1b9-129">INPUTS</span></span>

### <span data-ttu-id="be1b9-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be1b9-130">System.String</span></span>

## <span data-ttu-id="be1b9-131">출력</span><span class="sxs-lookup"><span data-stu-id="be1b9-131">OUTPUTS</span></span>

### <span data-ttu-id="be1b9-132">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="be1b9-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="be1b9-133">상속자</span><span class="sxs-lookup"><span data-stu-id="be1b9-133">NOTES</span></span>

## <span data-ttu-id="be1b9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be1b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="be1b9-135">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="be1b9-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="be1b9-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="be1b9-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="be1b9-137">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="be1b9-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="be1b9-138">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="be1b9-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

