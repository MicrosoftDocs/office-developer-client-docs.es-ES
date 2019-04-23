---
title: NextRecordset (método, ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288620"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset (método, ADO)

**Se aplica a:** Access 2013, Office 2013
 
Borra el objeto [Recordset](recordset-object-ado.md) actual y devuelve el siguiente objeto **Recordset** recorriendo varios comandos.

## <a name="syntax"></a>Sintaxis

Establecer *Recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto **Recordset**. En el modelo de sintaxis, * recordset1* y *recordset2* pueden ser el mismo objeto **Recordset**, o bien, pueden ser objetos independientes. Si utiliza objetos **Recordset** independientes y restablece el valor de la propiedad **ActiveConnection** en el objeto **Recordset** original (*recordset1*), se generará un error después de llamar a **NextRecordset**.

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*RecordsAffected* |Es opcional. Variable de tipo **Long** a la que el proveedor devuelve el número de registros afectados por la actual operación.|

> [!NOTE]
> [!NOTA] Este parámetro sólo devuelve el número de registros que se ven afectados por una operación; no devuelve un número de registros de una instrucción SELECT usada para generar el objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results. Si abre un objeto **Recordset** basado en una instrucción de comando compuesta (por ejemplo, "SELECT \* from Table1; SELECT \* from Tabla2 ") mediante el [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) método Execute en un [comando](command-object-ado.md) o el método [Open](open-method-ado-recordset.md) en un **objeto Recordset**, ADO ejecuta únicamente el primer comando y devuelve los resultados a un *objeto Recordset*. To access the results of subsequent commands in the statement, call the **NextRecordset** method.

Mientras haya resultados adicionales y el objeto **Recordset** que contiene las instrucciones compuestas no esté desconectado ni se hayan calculado las referencias de los límites del proceso, el método **NextRecordset** seguirá devolviendo objetos **Recordset**. Si un comando que devuelve filas se ejecuta correctamente pero no devuelve registros, el objeto **Recordset** devuelto estará abierto pero vacío. Para ver si este es el caso, compruebe si el valor de las propiedades [BOF](bof-eof-properties-ado.md) y [EOF](bof-eof-properties-ado.md) es **True**. Si un comando que no devuelve filas se ejecuta correctamente, el objeto **Recordset** devuelto estará cerrado, lo que puede comprobarse mediante la propiedad [State](state-property-ado.md) del objeto **Recordset**. Cuando ya no queden más resultados, el valor de *Recordset* será *Nothing*.

El método **NextRecordset** no está disponible en un objeto **Recordset** desconectado, donde el valor de [ActiveConnection](activeconnection-property-ado.md) es **Nothing** (en Microsoft Visual Basic) o NULL (en otros lenguajes).

Si hay una modificación en curso mientras se está en modo de actualización inmediata y se llama al método **NextRecordset**, se generará un error; llame primero al método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).

Para pasar parámetros para más de un comando en la instrucción compuesta rellenando la colección [Parameters](parameters-collection-ado.md), o bien, pasando una matriz con la llamada original a **Abrir** o **Execute**, los parámetros deben estar en el mismo orden en la colección o matriz que sus respectivos comandos en la serie de comandos. Es preciso terminar de leer todos los resultados antes de leer los valores de los parámetros de salida.

El proveedor OLE DB determina cuándo se ejecuta cada comando de una instrucción compuesta. Por ejemplo, el [proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md) ejecuta todos los comandos de un lote después de recibir la instrucción compuesta. Los objetos **Recordset** resultantes se devuelven simplemente al llamar a **NextRecordset**.

Sin embargo, puede que otros proveedores ejecuten el siguiente comando de una instrucción sólo después de una llamada a NextRecordset. En este caso, si cierra explícitamente el objeto **Recordset** antes de ejecutar paso a paso toda la instrucción de comandos, ADO no ejecutará nunca los comandos restantes.

