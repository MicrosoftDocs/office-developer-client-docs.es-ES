---
title: NumericScale (propiedad, ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288521"
---
# <a name="numericscale-property-adox"></a>NumericScale (propiedad, ADOX)


**Se aplica a:** Access 2013, Office 2013

Indica la escala de un valor numérico de la columna.

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece y devuelve un valor **Byte** que es la escala de valores de datos de la columna cuando la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) es **adNumeric** o **adDecimal**. **NumericScale** se omite para todos los demás tipos de datos.

## <a name="remarks"></a>Comentarios

El valor predeterminado es cero (0).

**NumericScale** es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.

