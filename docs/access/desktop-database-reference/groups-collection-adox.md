---
title: Groups (colección, ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712522"
---
# <a name="groups-collection-adox"></a>Groups (colección, ADOX)

**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [Group](group-object-adox.md) almacenados de un catálogo o un usuario.

## <a name="remarks"></a>Comentarios

La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.

El método [Append](append-method-adox-groups.md) de una colección **Groups** es único para ADOX. Se puede:

- Agregar un nuevo grupo de seguridad a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

- Tener acceso a un grupo de la colección con la propiedad [Item](item-property-ado.md).

- Devolver el número de grupos incluido en la colección con la propiedad [Count](count-property-ado.md).

- Quitar un grupo de la colección con el método [Delete](delete-method-adox-collections.md).

- Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

> [!NOTE]
> [!NOTA] Para poder anexar un objeto **Group** a la colección **Groups** de un objeto **User**, debe existir previamente un objeto **Group** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Groups** del **catálogo**.


