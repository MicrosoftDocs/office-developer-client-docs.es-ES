---
title: NumericScale (propiedad, ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4229a318c4eb855b86164f02f1075d29a915d718
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485575"
---
# <a name="numericscale-property-adox"></a>NumericScale (propiedad, ADOX)


**Se aplica a**: Access 2013 | Office 2013

Indica la escala de un valor numérico de la columna.

## <a name="settings-and-return-values"></a>Configuraciones y valores devueltos

Establece y devuelve un valor **Byte** que es la escala de valores de datos de la columna cuando la propiedad [Tipo](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) es **adNumeric** o **adDecimal**. **NumericScale** se omite para todos los demás tipos de datos.

## <a name="remarks"></a>Comentarios

El valor predeterminado es cero (0).

**NumericScale** es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.

