---
title: Append (método, Users de ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297070"
---
# <a name="append-method-adox-users"></a>Append (método, Users de ADOX)

**Se aplica a:** Access 2013, Office 2013

Agrega un nuevo objeto [User](user-object-adox.md) a la colección [Users](users-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Usuarios*. Append *User* \[ ,*Password*\]

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*User* |Un valor **Variant** que contiene el objeto **User** que se va a anexar o al nombre del usuario que se va a crear y anexar.|
|*Password* |Opcional. Un valor **String** que contiene la contraseña del usuario. El parámetro *Password* corresponde al valor especificado por el método [ChangePassword](changepassword-method-adox.md) de un objeto **User**.|

## <a name="remarks"></a>Comentarios

La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.

Si el proveedor no admite la creación de usuarios, se producirá un error.

> [!NOTE]
> [!NOTA] Para poder anexar un objeto **User** a la colección **Users** de un objeto **Group**, debe existir previamente un objeto **User** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Users** del **catálogo**.


