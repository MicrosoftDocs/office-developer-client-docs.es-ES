---
title: ChangePassword (método, ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296531"
---
# <a name="changepassword-method-adox"></a>ChangePassword (método, ADOX)

**Se aplica a:** Access 2013, Office 2013

Cambia la contraseña de una cuenta de usuario.

## <a name="syntax"></a>Sintaxis

*Usuario*. ChangePassword*OldPassword*, *newPassword*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*OldPassword* |Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.|
|*NewPassword* |Un valor **String** que especifica la nueva contraseña.|

## <a name="remarks"></a>Comentarios

Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.

Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.

