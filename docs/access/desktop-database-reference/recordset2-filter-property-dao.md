---
title: Propiedad Recordset2.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307332"
---
# <a name="recordset2filter-property-dao"></a>Propiedad Recordset2.Filter (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que determina los registros incluidos en un objeto **Recordset** abierto posteriormente (solo en áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expression* .Filter

*expresión* Expresión que devuelve un **objeto Recordset2.**

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos String que contiene la cláusula WHERE de una instrucción SQL sin la palabra reservada WHERE.

Use la propiedad **Filter** para aplicar un filtro a un objeto **Recordset** de tipo Dynaset, Snapshot o solo avance.

Puede usar la propiedad **Filter** para limitar los registros que se devuelven desde un objeto existente cuando un nuevo objeto **Recordset** se abre basado en un objeto **Recordset** existente.

Utilice el formato de fecha de Estados Unidos (mes-día-año) cuando filtre campos que contengan fechas, incluso si no está utilizando una versión de Estados Unidos del motor de base de datos Microsoft Access (en cuyo caso debe reunir cualquier fecha concatenando cadenas, por ejemplo, strMonth & "-" & strDay & "-" & strYear). De lo contrario, puede que no se filtren los datos de la forma esperada.

En mucho casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya una cláusula WHERE.

Si configura la propiedad en una cadena concatenada con un valor no entero y los parámetros del sistema especifican un carácter decimal distinto del estándar de Estados Unidos, como una coma (por ejemplo, strFilter = "PRICE \> " & lngPrice y lngPrice = 125,50), aparecerá un error cuando intente abrir el siguiente objeto **Recordset**. Esto se produce porque durante la concatenación, el número se convertirá en una cadena usando el carácter decimal predeterminado del sistema y Microsoft Access SQL solo acepta caracteres decimales con el formato estándar de Estados Unidos.

