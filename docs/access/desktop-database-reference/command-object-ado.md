---
title: Objeto Command (ADO)
TOCTitle: Command object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dc582046ff1981a82fab9c9c551b0064c1e8c1de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296174"
---
# <a name="command-object-ado"></a>Objeto Command (ADO)


**Se aplica a:** Access 2013, Office 2013

Define un comando específico que se intenta ejecutar con respecto a un origen de datos.

## <a name="remarks"></a>Comentarios

Use un objeto **Command** para realizar una consulta en una base de datos y devolver registros en un objeto [Recordset](recordset-object-ado.md), para ejecutar una operación masiva, o para manipular la estructura de una base de datos. Según la funcionalidad del proveedor, algunos métodos, colecciones o propiedades del objeto **Command** pueden generar un error cuando se hace referencia a ellos.

Con las colecciones, los métodos y las propiedades de un objeto **Command**, se puede hacer lo siguiente:

  - Definir el texto ejecutable del comando (por ejemplo, una instrucción SQL) con la propiedad [CommandText](commandtext-property-ado.md).

  - Definir consultas con parámetros o argumentos de procedimientos almacenados con objetos [Parameter](parameter-object-ado.md) y la colección [Parameters](parameters-collection-ado.md).

  - Ejecutar un comando y devolver un objeto **Recordset**, si procede, con el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

  - Especificar el tipo de comando con la propiedad [CommandType](commandtype-property-ado.md) antes de la ejecución para optimizar el rendimiento.

  - Controlar si el proveedor guarda una versión preparada (o compilada) del comando antes de la ejecución con la propiedad [Prepared](prepared-property-ado.md).

  - Establecer el número de segundos que esperará un proveedor para la ejecución de un comando con la propiedad [CommandTimeout](commandtimeout-property-ado.md).

  - Asociar una conexión abierta con un objeto **Command** estableciendo su propiedad [ActiveConnection](activeconnection-property-ado.md).

  - Establecer la propiedad [Name](name-property-ado.md) para identificar el objeto **Command** como un método en el objeto [Connection](connection-object-ado.md) asociado.

  - Pasar un objeto **Command** a la propiedad [Source](source-property-ado-recordset.md) de un objeto **Recordset** para obtener datos.

  - Obtener acceso a atributos específicos del proveedor con la colección [Properties](properties-collection-ado.md).

> [!NOTE]
> [!NOTA] Para ejecutar una consulta sin usar un objeto **Command**, pase una cadena de consulta al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de un objeto **Connection** o al método [Open](open-method-ado-recordset.md) de un objeto **Recordset**. Sin embargo, un objeto **Command** es necesario cuando quiere conservar el texto del comando y volver a ejecutarlo o usar parámetros de consulta.

Para crear un objeto **Command** independientemente de un objeto **Connection** definido anteriormente, establezca su propiedad **ActiveConnection** en una cadena de conexión válida. ADO seguirá creando un objeto **Connection**, pero no asignará ese objeto a una variable de objeto. Sin embargo, si asocia varios objetos **Command** a la misma conexión, debe crear y abrir explícitamente un objeto **Connection**; de este modo, se asigna el objeto **Connection** a una variable de objeto. Si no establece la propiedad **ActiveConnection** del objeto **Command** en esta variable de objeto, ADO creará un nuevo objeto **Connection** para cada objeto **Command**, aunque se utilice la misma cadena de conexión.

Para ejecutar un objeto **Command**, basta con invocarlo mediante su propiedad [Name](name-property-ado.md) en el objeto **Connection** asociado. El objeto **Command** debe tener su propiedad **ActiveConnection** establecida en el objeto **Connection**. Si el objeto **Command** tiene parámetros, pase como argumentos sus correspondientes valores al método.

Si se ejecutan dos o más objetos **Command** en la misma conexión y cualquiera de los objetos **Command** es un procedimiento almacenado con parámetros de salida, se producirá un error. Para ejecutar cada uno de los objetos **Command**, use conexiones independientes o desconecte todos los demás objetos **Command** de la conexión.

La colección **Parameters** es el miembro predeterminado del objeto **Command**. Como consecuencia, las dos instrucciones de código siguientes son equivalentes.

