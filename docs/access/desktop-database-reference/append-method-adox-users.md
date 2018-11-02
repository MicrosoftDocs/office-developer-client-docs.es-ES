---
title: Append (método, Users de ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b03bb74c5442eba3e1794d8067fa709f68af3d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931368"
---
# <a name="append-method-adox-users"></a>Append (método, Users de ADOX)


**Se aplica a**: Access 2013, Office 2013


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
> [!NOTA] Para poder anexar un objeto **User** a la colección **Users** de un objeto **Group**, debe existir previamente un objeto **User** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Users** del **catálogo**.


