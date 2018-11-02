---
title: Objeto Error - ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6a18570071428bfbd92d6674ca281234ea883bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925215"
---
# <a name="error-object-ado"></a>Error (objeto, ADO)


**Se aplica a**: Access 2013, Office 2013

Contiene detalles sobre errores de acceso a datos relacionados con una operación única que implica al proveedor.

## <a name="remarks"></a>Comentarios

Toda operación que implique a objetos de ADO puede generar errores relacionados con el proveedor. Cuando se produce alguno de estos errores, se colocan objetos **Error** en la colección [Errors](errors-collection-ado.md) del objeto [Connection](connection-object-ado.md). Cuando otra operación ADO genera un error, se borra la colección **Errors** y el nuevo conjunto de objetos **Error** se coloca en la colección **Errors**.

> [!NOTE]
> [!NOTA] Cada objeto **Error** representa un error de proveedor específico, no un error de ADO. Los errores de ADO se exponen al mecanismo de control de excepciones en tiempo de ejecución. Por ejemplo, en Microsoft Visual Basic, la generación de un error específico de ADO desencadenará un evento **On Error** y aparecerá el objeto **Error**. Para obtener una lista completa de errores de ADO, vea el tema correspondiente a [ErrorValueEnum](errorvalueenum.md).

Puede leer las propiedades de un objeto **Error** para obtener detalles específicos de cada error, como por ejemplo:

- La propiedad [Description](description-property-ado.md), que contiene el texto del error. Esta es la propiedad predeterminada.

- La propiedad [Number](number-property-ado.md), que contiene al valor entero de tipo **Long** de la constante del error.

- La propiedad [Source](source-property-ado-error.md), que identifica el objeto que generó el error. Esto es sumamente útil cuando se tienen varios objetos **Error** en la colección **Errors** tras realizar una solicitud a un origen de datos.

- Las propiedades [SQLState](sqlstate-property-ado.md) y [NativeError](nativeerror-property-ado.md), que proporcionan información de orígenes de datos SQL.

Cuando se produce un error de proveedor, se coloca en la colección **Errors** del objeto **Connection**. ADO admite la devolución de varios errores mediante una única operación de ADO para proporcionar información específica de errores al proveedor. Para obtener esta valiosa información de errores en un controlador de errores, utilice las características de intercepción de errores apropiadas del lenguaje o del entorno con el que está trabajando y, a continuación, use bucles anidados para enumerar las propiedades de cada objeto **Error** de la colección **Errors**.

**Microsoft Visual Basic y VBScript a los usuarios** Si no hay ningún objeto **Connection** válido, debe recuperar información de errores desde el objeto **Error** .

Del mismo modo que hacen los proveedores, ADO borra el objeto **OLE Error Info** antes de realizar una llamada que pueda generar un nuevo error de proveedor. Sin embargo, la colección **Errors** del objeto **Connection** se borra y se rellena sólo cuando el proveedor genera un nuevo error, o cuando se llama al método [Clear](clear-method-ado.md).

Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto **Connection**, y antes de establecer la propiedad [Filter](filter-property-ado.md) en un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si se devuelven advertencias.

