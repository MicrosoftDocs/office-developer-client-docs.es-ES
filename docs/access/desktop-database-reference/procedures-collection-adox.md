---
title: Colección Procedures (ADOX)
TOCTitle: Procedures collection (ADOX)
ms:assetid: e1ca53ad-1213-b514-e015-e18c2ab15e23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250150(v=office.15)
ms:contentKeyID: 48548267
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7bded8a6d0e6f2a4907977f32c8c37301ab323
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301361"
---
# <a name="procedures-collection-adox"></a>Colección Procedures (ADOX)


**Se aplica a:** Access 2013, Office 2013

Contiene todos los objetos [Procedure](procedure-object-adox.md) de un catálogo.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-procedures.md) de una colección **Procedures** es único para ADOX. Se puede:

  - Agregar un nuevo procedimiento a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a un procedimiento de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de procedimientos incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar un procedimiento de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

