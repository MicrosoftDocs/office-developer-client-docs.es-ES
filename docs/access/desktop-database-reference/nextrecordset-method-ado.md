---
title: NextRecordset (método, ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec6b6677e0de89b22f3c35009edcbc05684d10ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872602"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset (método, ADO)


**Se aplica a**: Access 2013, Office 2013
 

Borra el objeto [Recordset](recordset-object-ado.md) actual y devuelve el siguiente objeto **Recordset** recorriendo varios comandos.

## <a name="syntax"></a>Sintaxis

Establecer *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto **Recordset**. En el modelo de sintaxis, * recordset1* y *recordset2* pueden ser el mismo objeto **Recordset**, o bien, pueden ser objetos independientes. Si utiliza objetos **Recordset** independientes y restablece el valor de la propiedad **ActiveConnection** en el objeto **Recordset** original (*recordset1*), se generará un error después de llamar a **NextRecordset**.

## <a name="parameters"></a>Parámetros

- *RecordsAffected*

- Es opcional. Variable de tipo **Long** a la que el proveedor devuelve el número de registros afectados por la actual operación.


> [!NOTE]
> <P>[!NOTA] Este parámetro sólo devuelve el número de registros que se ven afectados por una operación; no devuelve un número de registros de una instrucción SELECT usada para generar el objeto <STRONG>Recordset</STRONG>.</P>



## <a name="remarks"></a>Comentarios

Utilice el método **NextRecordset** para devolver los resultados del siguiente comando en una instrucción de comando compuesta o de un procedimiento almacenado que devuelve varios resultados. Si abre un objeto **Recordset** basado en una instrucción de comando compuesta (por ejemplo, "seleccione \* FROM Tabla1; Seleccione \* FROM Tabla2 ") mediante el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) en un [comando](command-object-ado.md) o el método [Open](open-method-ado-recordset.md) en un **objeto Recordset**, ADO ejecuta sólo el primer comando y devuelve los resultados al *objeto recordset*. Para obtener acceso a los resultados de los comandos subsiguientes de la instrucción, llame al método **NextRecordset** .

Mientras haya resultados adicionales y el objeto **Recordset** que contiene las instrucciones compuestas no esté desconectado ni se hayan calculado las referencias de los límites del proceso, el método **NextRecordset** seguirá devolviendo objetos **Recordset**. Si un comando que devuelve filas se ejecuta correctamente pero no devuelve registros, el objeto **Recordset** devuelto estará abierto pero vacío. Para ver si este es el caso, compruebe si el valor de las propiedades [BOF](bof-eof-properties-ado.md) y [EOF](bof-eof-properties-ado.md) es **True**. Si un comando no devuelve filas se ejecuta correctamente, el objeto **Recordset** devuelto estará cerrado, lo que puede comprobarse mediante la propiedad [State](state-property-ado.md) en el **conjunto de registros**. Cuando no hay ningún resultado más, *recordset* se establecerá en *Nothing*.

El método **NextRecordset** no está disponible en un objeto **Recordset** desconectado, donde el valor de [ActiveConnection](activeconnection-property-ado.md) es **Nothing** (en Microsoft Visual Basic) o NULL (en otros lenguajes).

Si hay una modificación en curso mientras se está en modo de actualización inmediata y se llama al método **NextRecordset**, se generará un error; llame primero al método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).

Para pasar parámetros para más de un comando en la instrucción compuesta rellenando la colección [Parameters](parameters-collection-ado.md), o bien, pasando una matriz con la llamada original a **Abrir** o **Execute**, los parámetros deben estar en el mismo orden en la colección o matriz que sus respectivos comandos en la serie de comandos. Es preciso terminar de leer todos los resultados antes de leer los valores de los parámetros de salida.

El proveedor OLE DB determina cuándo se ejecuta cada comando de una instrucción compuesta. Por ejemplo, el [proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md) ejecuta todos los comandos de un lote después de recibir la instrucción compuesta. Los objetos **Recordset** resultantes se devuelven simplemente al llamar a **NextRecordset**.

Sin embargo, puede que otros proveedores ejecuten el siguiente comando de una instrucción sólo después de una llamada a NextRecordset. En este caso, si cierra explícitamente el objeto **Recordset** antes de ejecutar paso a paso toda la instrucción de comandos, ADO no ejecutará nunca los comandos restantes.

