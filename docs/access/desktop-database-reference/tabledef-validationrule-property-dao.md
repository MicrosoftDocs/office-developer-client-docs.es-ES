---
title: TableDef.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d396c830ecaffd1f1c2d8d57f509baaa9171ae9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486804"
---
# <a name="tabledefvalidationrule-property-dao"></a>TableDef.ValidationRule Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationRule

*expresión* Variable que representa un objeto **TableDef** .

## <a name="remarks"></a>Observaciones

La configuración o los valores devueltos son de tipo **String** que describe una comparación en el formulario de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.

La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error en tiempo de ejecución capturable. El mensaje de error devuelto es el texto de la propiedad **ValidationText**, si se especifica, o el texto de la expresión especificada por **ValidationRule**.

La validación sólo se admite para bases de datos que usan el motor de base de datos de Microsoft Access.

La expresión de cadena especificada por la propiedad **ValidationRule** de un objeto **Field** puede referirse sólo a ese **Field**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar a **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.

La propiedad **ValidationRule** de un objeto **Recordset** o **TableDef** puede hacer referencia a varios campos de ese objeto. Son de aplicación las restricciones señaladas anteriormente en este tema para el objeto **Field**.

Para un objeto **TableDef** basado en una tabla vinculada, la propiedad **ValidationRule** hereda el valor de la propiedad **ValidationRule** de la tabla base subyacente. Si la tabla base subyacente no admite la validación, el valor de esta propiedad es una cadena de longitud cero ("").


> [!NOTE]
> <P>Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos. Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</P>


