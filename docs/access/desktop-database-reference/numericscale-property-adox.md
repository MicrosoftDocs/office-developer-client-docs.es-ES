---
title: NumericScale (propiedad, ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7dd53830216c302d68adf44e1bea88bbc52e980
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921316"
---
# <a name="numericscale-property-adox"></a>NumericScale (propiedad, ADOX)


**Se aplica a**: Access 2013, Office 2013

Indica la escala de un valor numérico de la columna.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece y devuelve un valor **Byte** que es la escala de valores de datos de la columna cuando la propiedad [Tipo](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) es **adNumeric** o **adDecimal**. **NumericScale** se omite para todos los demás tipos de datos.

## <a name="remarks"></a>Comentarios

El valor predeterminado es cero (0).

**NumericScale** es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.

