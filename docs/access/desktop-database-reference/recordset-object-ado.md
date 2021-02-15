---
title: Objeto Recordset (ADO)
TOCTitle: Recordset object (ADO)
ms:assetid: 0f963bf8-f066-dc8a-b754-f427de712df1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248865(v=office.15)
ms:contentKeyID: 48543267
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 636681cf8e0c20f078387b21974141a9cb66cfcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300479"
---
# <a name="recordset-object-ado"></a>Objeto Recordset (ADO)

**Se aplica a:** Access 2013, Office 2013

Representa el conjunto completo de registros de una tabla base o los resultados de un comando ejecutado. En cualquier momento, el objeto **Recordset** hace referencia sólo a un único registro dentro del conjunto como registro actual.

## <a name="remarks"></a>Comentarios

Los objetos **Recordset** se usan para manipular datos de un proveedor. Cuando se usa ADO, los datos se manipulan en su práctica totalidad mediante el uso de objetos **Recordset**. Todos los objetos **Recordset** constan de registros (filas) y campos (columnas). Según la funcionalidad compatible con el proveedor, algunas propiedades o métodos de **Recordset** pueden no estar disponibles.

ADODB.Recordset es el identificador de programa (ProgID) que se debe usar para crear un objeto **Recordset**. Las aplicaciones existentes que hacen referencia al identificador de programa (ProgID) ADOR.Recordset obsoleto continuarán funcionando sin recompilar, pero el nuevo desarrollo debe hacer referencia a ADODB.Recordset.

Hay cuatro tipos diferentes de cursor definidos en ADO:

  - **Cursor dinámico**: permite ver adiciones, modificaciones y eliminaciones efectuadas por otros usuarios; permite todos los tipos de movimiento en el objeto **Recordset** que no estén basados en marcadores y permite la presencia de marcadores si el proveedor los admite.

  - **Cursor estático de claves**: se comporta como un cursor dinámico, con la excepción de que impide ver los registros agregados por otros usuarios, así como el acceso a los registros eliminados por otros usuarios. Las modificaciones en los datos realizadas por otros usuarios seguirán siendo visibles. Siempre admite marcadores y, por lo tanto, permite todos los tipos de movimiento en el objeto **Recordset**.

  - **Cursor estático**: proporciona una copia estática de un conjunto de registros para su utilización con el fin de buscar datos o generar informes; siempre admite marcadores y, por lo tanto, permite todos los tipos de movimiento en el objeto **Recordset**. Las adiciones, modificaciones o eliminaciones realizadas por otros usuarios no serán visibles. Este es el único tipo de cursor permitido cuando se abre un objeto **Recordset** del cliente.

  - **Cursor de sólo avance**: permite sólo el desplazamiento hacia delante en el objeto **Recordset**. Las adiciones, modificaciones o eliminaciones realizadas por otros usuarios no serán visibles. Este cursor mejora el rendimiento cuando sólo se necesita recorrer un objeto **Recordset** una vez.

Establezca la propiedad [CursorType](cursortype-property-ado.md) antes de abrir el objeto **Recordset** para elegir el tipo de cursor, o pase un argumento *CursorType* con el método [Open](open-method-ado-recordset.md). Algunos proveedores no admiten todos los tipos de cursor. Compruebe la documentación del proveedor. Si no especifica un tipo de cursor, ADO abrirá de forma predeterminada un cursor de sólo avance.

Si la propiedad [CursorLocation](cursorlocation-property-ado.md) se establece en **adUseClient** para abrir un objeto **Recordset**, la propiedad **UnderlyingValue** de objetos [Field](field-object-ado.md) no estará disponible en el objeto **Recordset** devuelto. Cuando se usa con algunos proveedores (como el proveedor ODBC de Microsoft para OLE DB conjuntamente con Microsoft SQL Server), se pueden crear objetos **Recordset** independientemente del objeto [Connection](connection-object-ado.md) definido anteriormente si se pasa una cadena de conexión con el método **Open**. ADO seguirá creando un objeto [Connection](connection-object-ado.md), pero no asignará ese objeto a una variable de objeto. Sin embargo, si se abren varios objetos **Recordset** con la misma conexión, se debe crear y abrir explícitamente un objeto **Connection**; de este modo, se asigna el objeto **Connection** a una variable de objeto. Si no se usa esta variable de objeto al abrir los objetos **Recordset**, ADO creará un nuevo objeto **Connection** para cada nuevo objeto **Recordset**, aunque se pase la misma cadena de conexión.

Puede crear todos los objetos **Recordset** que necesite.

Cuando se abre un objeto **Recordset**, el registro actual se coloca en el primer registro (si existe) y las propiedades [BOF](bof-eof-properties-ado.md) y [EOF](bof-eof-properties-ado.md) se establecen en **False**. Si no hay registros, los valores de las propiedades **BOF** y **EOF** son **True**.

Puede usar los métodos [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), **MoveLast**, **MoveNext** y **MovePrevious**; el método [Move](move-method-ado.md); y las propiedades [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) y [Filter](filter-property-ado.md) para volver a colocar el registro actual, suponiendo que el proveedor admita la funcionalidad pertinente. Los objetos **Recordset** de solo avance admiten únicamente el método [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). Cuando use los métodos **Move** para visitar cada registro (o enumerar el objeto **Recordset**), puede usar las propiedades **BOF** y **EOF** para determinar si se ha desplazado más allá del principio o el final del objeto **Recordset**.

Los objetos **Recordset** pueden admitir dos tipos de actualizaciones: inmediata y por lotes. En la actualización inmediata, todas las modificaciones efectuadas en datos se escriben inmediatamente en el origen de datos subyacente cuando se llama al método [Update](update-method-ado.md). También se pueden pasar matrices de valores como parámetros con los métodos [AddNew](addnew-method-ado.md) y **Update**, y actualizar simultáneamente varios campos de un registro.

Si un proveedor admite la actualización por lotes, puede hacer que la caché del proveedor cambie a varios registros y transmitirlos a continuación en una única llamada a la base de datos con el método [UpdateBatch](updatebatch-method-ado.md). Esto es aplicable a las modificaciones efectuadas con los métodos **AddNew**, **Update** y [Delete](delete-method-ado-recordset.md). Después de llamar al método **UpdateBatch**, puede usar la propiedad [Status](status-property-ado-recordset.md) para comprobar la existencia de conflictos de datos con el fin de resolverlos.

> [!NOTE]
> [!NOTA] Para ejecutar una consulta sin usar un objeto [Command](command-object-ado.md), pase una cadena de consulta al método **Open** de un objeto **Recordset**. Sin embargo, se requiere un objeto **Command** cuando se desea conservar el texto del comando y volver a ejecutarlo, o usar parámetros de consulta.

La propiedad [Mode](mode-property-ado.md) controla los permisos de acceso.

La colección **Fields** es el miembro predeterminado del objeto **Recordset**. Como consecuencia, las dos instrucciones de código siguientes son equivalentes.

```vb
    Debug.Print objRs.Fields.Item(0)  ' Both statements print 
    Debug.Print objRs(0)              '  the Value of Item(0).
```
