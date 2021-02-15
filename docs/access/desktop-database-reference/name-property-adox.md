---
title: Propiedad Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288654"
---
# <a name="name-property-adox"></a>Propiedad Name (ADOX)

**Se aplica a:** Access 2013, Office 2013

Indica el nombre del objeto.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String**.

## <a name="remarks"></a>Comentarios

Los nombres no tienen por qué ser únicos dentro de una colección.

La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).

Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").

> [!NOTE]
> - Para claves, esta propiedad es de sólo lectura en objetos **Key** ya anexados a una colección.
> - [!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos **Table** ya anexados a una colección.


