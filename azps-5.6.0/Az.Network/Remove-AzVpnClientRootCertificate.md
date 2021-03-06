---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005904"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
기존 VPN 클라이언트 루트 인증서를 제거합니다.

## 구문

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Remove-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 지정된 루트 인증서를 제거합니다.
루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다. 게이트웨이에서 사용되는 다른 모든 인증서는 루트 인증서를 신뢰합니다.
인증 목적으로 인증서를 사용하는 루트 인증서 컴퓨터를 제거하면 게이트웨이에 더 이상 연결할 수 없습니다.
**Remove-AzVpnClientRootCertificate를** 사용하는 경우 인증서 이름과 인증서 데이터의 텍스트 표현을 모두 제공해야 합니다.
인증서의 텍스트 표현에 대한 자세한 내용은 *PublicCertData 매개* 변수 설명을 참조하세요.

## 예제

### 예제 1: 가상 네트워크 게이트웨이에서 클라이언트 루트 인증서 제거
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

이 예제에서는 가상 네트워크 게이트웨이 ContosoVirtualGateway에서 ContosoRootCertificate라는 클라이언트 루트 인증서를 제거합니다.
첫 번째 명령은 **Get-Content** cmdlet을 사용하여 이전에 내보낼 인증서의 텍스트 표현을 얻게 됩니다. 이 텍스트 표현은 이라는 변수에 $Text.
그런 다음 두 번째 명령은 for loop를 사용하여 첫 번째 줄과 $Text 제외한 모든 텍스트를 추출합니다.
이 추출된 텍스트는 이라는 변수에 $CertificateText.
세 번째 명령은 **Remove-AzVpnClientRootCertificate** cmdlet과 함께 $CertificateText 변수에 저장된 정보를 사용하여 게이트웨이에서 인증서를 제거합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -PublicCertData
제거할 루트 인증서의 텍스트 표현을 지정합니다.
텍스트 표현을 얻었다면 .cer 형식(Base64 사용) 인코딩으로 인증서를 내보내고 결과 파일을 텍스트 편집기에서 니다.
다음과 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 많은 텍스트 줄이 포함되어 있습니다 -----. MIIC13FAAXC3671Auij9HHhgUNEW8343NMJklo에서 BEGIN CERTIFICATE ----- 09982CVVFAw8w ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 -----.
"$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText =($i=1; $i -lt $Text.length -1 ; $i+){$Text+){$i } Windows PowerShell \[ \]

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

### -ResourceGroupName
가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.
리소스 그룹은 인벤토리 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.

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

### -VirtualNetworkGatewayName
인증서가 제거된 가상 네트워크 게이트웨이의 이름을 지정합니다.

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

### -VpnClientRootCertificateName
이 cmdlet이 제거하는 클라이언트 루트 인증서의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


