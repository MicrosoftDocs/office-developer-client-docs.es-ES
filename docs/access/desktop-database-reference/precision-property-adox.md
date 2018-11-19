---
title: Precision (propiedad, ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 973e5e3a6d9c61a0fdc6b259a8a7b846b62af6fd
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026109"
---
# <a name="precision-property-adox"></a>Precision (propiedad, ADOX)


**Se aplica a**: Access 2013, Office 2013

Indica la precisión máxima de los valores de datos de la columna.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece y devuelve un valor **Long** que es la precisión máxima de valores de datos de la columna cuando la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) es un tipo numérico. **Precision** se omite para todos los demás tipos de datos.

## <a name="remarks"></a>Comentarios

El valor predeterminado es cero (0).

Esta propiedad es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.

