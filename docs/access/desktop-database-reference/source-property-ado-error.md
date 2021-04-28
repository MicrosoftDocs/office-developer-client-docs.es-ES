---
title: Source (propiedad, Error de ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061314"
---
# <a name="source-property-ado-error"></a>Source (propiedad, Error de ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el nombre del objeto o de la aplicación que ha generado un error originariamente.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **String** que indica el nombre de un objeto o una aplicación.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Source** de un objeto [Error](error-object-ado.md) para determinar el nombre del objeto o la aplicación que ha generado un error. Puede ser el nombre de clase o el Id. de programación del objeto. En los errores de ADO, el valor de la propiedad será **ADODB.** *ObjectName*, donde *ObjectName* es el nombre del objeto que ha desencadenado el error. En ADOX y ADO MD, el valor será **ADOX.** *ObjectName* y **ADOMD.** *ObjectName,* respectivamente.

Basándose en la documentación del error de las propiedades **Source**, [Number](number-property-ado.md) y [Description](description-property-ado.md) de los objetos **Error**, es posible escribir código que controle el error de forma adecuada.

La propiedad **Source** es de sólo lectura para objetos **Error**.

