---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 675107a27774cf2fe44ef328cdb0d7a3569e8abb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952491"
---
# Remove-AzKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에서 비밀을 삭제합니다.

## 구문

### ByVaultName(기본값)
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Remove-AzKeyVaultSecret cmdlet은 키 자격 증명 모음에서 비밀을 삭제합니다.
비밀이 실수로 삭제된 경우 특별한 '복구' 권한이 Undo-AzKeyVaultSecretRemoval 사용자가 비밀을 사용하여 복구할 수 있습니다.
이 cmdlet에는 **ConfirmImpact** 속성에 대한 값이 높습니다.

## 예제

### 예제 1: 키 자격 증명 모음에서 비밀 제거
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 제거합니다.

### 예제 2: 사용자 확인 없이 키 자격 증명 모음에서 비밀 제거
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 제거합니다.
명령은 *힘* 및 확인  매개 변수를 지정하므로 cmdlet에서 확인을 요청하지 않습니다.

### 예제 3: 키 자격 증명 모음에서 삭제된 비밀을 영구적으로 제거합니다.
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 영구적으로 미리 제공합니다.
이 cmdlet을 실행하려면 이 키 자격 증명 모음에 대해 사용자에게 이전에 명시적으로 부여된 '제거' 권한이 필요합니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -InputObject
Key Vault 비밀 개체

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
있는 경우 이전에 삭제한 비밀을 영구적으로 제거합니다.

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

### -Name
비밀의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 비밀의 완전히 자격을 갖춘 도메인 이름(FQDN)을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
이 cmdlet은 **Microsoft.Azure.Commands.KeyVault.Models.Secret 개체를 반환합니다.**
기본적으로 이 cmdlet은 출력을 생성하지 않습니다.

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

### -VaultName
비밀이 속한 키 자격 증명 모음의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 이름과 현재 환경을 기반으로 키 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecret

## 참고 사항

## 관련 링크

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Undo-AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

