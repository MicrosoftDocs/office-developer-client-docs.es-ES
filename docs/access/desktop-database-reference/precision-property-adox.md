---
title: Propiedad Precision (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287492"
---
# <a name="precision-property-adox"></a>Propiedad Precision (ADOX)


**Se aplica a:** Access 2013, Office 2013

Indica la precisión máxima de los valores de datos de la columna.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece y devuelve un valor **Long** que es la precisión máxima de valores de datos de la columna cuando la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) es un tipo numérico. **Precision** se omite para todos los demás tipos de datos.

## <a name="remarks"></a>Comentarios

El valor predeterminado es cero (0).

Esta propiedad es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.

