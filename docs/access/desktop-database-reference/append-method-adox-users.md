---
title: Append (método, usuarios ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484130"
---
# <a name="append-method-adox-users"></a>Append (método, usuarios ADOX)


**Se aplica a**: Access 2013 | Office 2013


Agrega un nuevo objeto [User](user-object-adox.md) a la colección [Users](users-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Los usuarios*. Anexe el*usuario*\[,*contraseña*\]

## <a name="parameters"></a>Parámetros

  - *User*

  - Un valor **Variant** que contiene el objeto **User** que se va a anexar o al nombre del usuario que se va a crear y anexar.

  - *Password*

  - Opcional. Un valor **String** que contiene la contraseña del usuario. El parámetro *Password* corresponde al valor especificado por el método [ChangePassword](changepassword-method-adox.md) de un objeto de **usuario** .

## <a name="remarks"></a>Comentarios

La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.

Si el proveedor no admite la creación de usuarios, se producirá un error.


> [!NOTE]
> <P>[!NOTA] Para poder anexar un objeto <STRONG>User</STRONG> a la colección <STRONG>Users</STRONG> de un objeto <STRONG>Group</STRONG>, debe existir previamente un objeto <STRONG>User</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Users</STRONG> del <STRONG>catálogo</STRONG>.</P>


