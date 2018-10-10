---
title: ChangePassword (método, ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483668"
---
# <a name="changepassword-method-adox"></a>ChangePassword (método, ADOX)


**Se aplica a**: Access 2013 | Office 2013



Cambia la contraseña de una cuenta de usuario.

## <a name="syntax"></a>Sintaxis

*Usuario*. ChangePassword*contraseñaAntigua*, *nuevaContraseña*

## <a name="parameters"></a>Parámetros

  - *ContraseñaAntigua*

  - Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.

  - *NewPassword*

  - Un valor **String** que especifica la nueva contraseña.

## <a name="remarks"></a>Comentarios

Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.

Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.

