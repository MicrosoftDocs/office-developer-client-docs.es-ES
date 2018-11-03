---
title: Source (propiedad, Recordset de ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a58ac3c5315daef040ba6a999753a19f76504087
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947576"
---
# <a name="source-property-ado-recordset"></a>Source (propiedad, Recordset de ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el origen de datos de un objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece un valor de tipo **String** o una referencia al objeto [Command](command-object-ado.md); sólo devuelve un valor de tipo **String** que indica el origen del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Source** para especificar un origen de datos para un objeto **Recordset** mediante uno de los siguientes: una variable de objeto **Command**, una instrucción SQL, un procedimiento almacenado o un nombre de tabla.

Si se establece la propiedad **Source** en un objeto **Command**, la propiedad [ActiveConnection](activeconnection-property-ado.md) del objeto **Recordset** heredará el valor de la propiedad **ActiveConnection** para el objeto **Command** especificado. No obstante, la lectura de la propiedad **Source** no devuelve un objeto **Command**; por el contrario, devuelve la propiedad [CommandText](commandtext-property-ado.md) del objeto **Command** en el que se ha establecido la propiedad **Source**.

Si la propiedad **Source** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla, puede optimizar el rendimiento, se pasa el argumento *Options* adecuado con la llamada al método [Open](open-method-ado-recordset.md) .

La propiedad **Source** es de lectura y escritura para los objetos **Recordset** cerrados y de sólo lectura para los objetos **Recordset** abiertos.

