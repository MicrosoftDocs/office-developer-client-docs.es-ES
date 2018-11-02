---
title: Name (propiedad, ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931249"
---
# <a name="name-property-adox"></a>Name (propiedad, ADOX)


**Se aplica a**: Access 2013, Office 2013

Indica el nombre del objeto.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String**.

## <a name="remarks"></a>Comentarios

Los nombres no tienen por qué ser únicos dentro de una colección.

La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).

Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").


> [!NOTE]
> <P>[!NOTA] Para claves, esta propiedad es de sólo lectura en objetos <STRONG>Key</STRONG> ya anexados a una colección.</P>




> [!NOTE]
> <P>[!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos <STRONG>Table</STRONG> ya anexados a una colección.</P>


