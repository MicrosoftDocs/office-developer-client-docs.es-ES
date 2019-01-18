---
title: Views (colección, ADOX)
TOCTitle: Views collection (ADOX)
ms:assetid: 8d0f9517-4be1-be9c-d4cd-6d50cd5a8983
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249618(v=office.15)
ms:contentKeyID: 48546246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ce9986d486eb76046216aabbce6352280042910
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719501"
---
# <a name="views-collection-adox"></a>Views (colección, ADOX)


**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [View](view-object-adox.md) de un catálogo.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-views.md) de una colección **Views** es único para ADOX. Se puede:

  - Agregar una nueva vista a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a una vista de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de vistas incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar una vista de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

