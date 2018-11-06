---
title: DBEngine.Idle (método) (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f94d869cd04dc0b16e0b428abaf60e4be32dacb7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998059"
---
# <a name="dbengineidle-method-dao"></a>DBEngine.Idle (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Suspende el procesamiento de datos y habilita el motor de base de datos de Microsoft Access para que realice las tareas pendientes, como la optimización de memoria o los tiempos de espera de paginación (sólo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Inactivo (***acción***)

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Acción</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica la acción que se va a realizar. Puede ser una de las constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El método **Idle** permite que el motor de base de datos de Microsoft Access realice tareas en segundo plano que pueden no estar actualizadas debido al procesamiento de una gran cantidad de datos. Esto suele ocurrir en los entornos multitarea y multiusuario que no disponen de tiempo de procesamiento en segundo plano suficiente para mantener todos los registros en un objeto **[Recordset](recordset-object-dao.md)** actual.

Normalmente, se quitan los bloqueos de lectura y los datos de los objetos **Recordset** locales de tipo dynaset solo se actualizan cuando no se produce ninguna otra acción (ni siquiera movimientos del mouse). Si usa con frecuencia el método **Idle**, el motor de base de datos de Microsoft Access puede ocuparse de las tareas de procesamiento en segundo plano liberando bloqueos de lectura innecesarios.

Al especificar el argumento **dbRefreshCache** opcional, la memoria se actualiza solamente con los datos más actuales de la base de datos.

No es necesario utilizar este método en entornos de un solo usuario a no ser que se ejecuten varias instancias de una aplicación. El método puede **Idle** mejorar el rendimiento en un entorno multiusuario, ya que fuerza al motor de base de datos a escribir datos en disco liberando bloqueos de la memoria.


> [!NOTE]
> [!NOTA] Puede liberar también bloqueos de lectura convirtiendo las operaciones en parte de una transacción.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza el método **Idle** para garantizar que un procedimiento de salida tiene acceso a los datos más actuales disponibles de la base de datos. Se requiere el procedimiento IdleOutput para que pueda ejecutarse este procedimiento.

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

