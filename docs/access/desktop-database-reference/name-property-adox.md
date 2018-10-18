---
title: Name (propiedad, ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604053"
---
# <a name="name-property-adox"></a>Name (propiedad, ADOX)


**Se aplica a**: Access 2013 | Office 2013

Indica el nombre del objeto.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String**.

## <a name="remarks"></a>Comentarios

Los nombres no tienen por qué ser únicos dentro de una colección.

La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).

Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").


> [!NOTE]
> <P>[!NOTA] Para claves, esta propiedad es de sólo lectura en objetos <STRONG>Key</STRONG> ya anexados a una colección.</P>




> [!NOTE]
> <P>[!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos <STRONG>Table</STRONG> ya anexados a una colección.</P>


