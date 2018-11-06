---
title: Recordset.FindFirst (método) (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 489e6060fdbaa4183c006e3f422c207d9a5013ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998857"
---
# <a name="recordsetfindfirst-method-dao"></a>Recordset.FindFirst (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Busca el primer registro de un objeto **Recordset** de tipo Dynaset o instantánea que satisfaga los criterios especificados y convierte el registro en el registro actual (solo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . FindFirst (***criterios***)

*expresión* Variable que representa un objeto **Recordset** .

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
<td><p><em>Criteria</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Cadena que se utiliza para localizar el registro. Es como una cláusula WHERE en una instrucción SQL pero sin la palabra WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Si quiere incluir en la búsqueda todos los registros, y no solo los que cumplan una condición determinada, use los métodos **Move** para moverse de un registro a otro. Para buscar un registro en un **Recordset** de tipo tabla, use el método **Seek**.

Si no se encuentra ningún registro que coincida con los criterios, el puntero del registro actual será desconocido y la propiedad **NoMatch** se configurará como **True**. Si el conjunto de registros contiene varios registros que cumplen los criterios, **FindFirst** buscará el primero, **FindNext** buscará el segundo y así sucesivamente.

Cada método **Find** empieza a buscar a partir de la ubicación y en la dirección que se especifican en la tabla siguiente.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método Find</p></th>
<th><p>Empieza la búsqueda en</p></th>
<th><p>Dirección de búsqueda</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Principio del conjunto de registros</p></td>
<td><p>Final del conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Final del conjunto de registros</p></td>
<td><p>Principio del conjunto de registros</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Registro actual</p></td>
<td><p>Final del conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Registro actual</p></td>
<td><p>Principio del conjunto de registros</p></td>
</tr>
</tbody>
</table>


No obstante, el uso de uno de los métodos **Find** no es igual a utilizar el método **Move**, que activa simplemente el registro primero, último, siguiente o anterior sin especificar una condición. Puede proseguir una operación Find con una operación Move.

Compruebe siempre el valor de la propiedad **NoMatch** para determinar si la operación Find se ha realizado correctamente. Si la búsqueda es correcta, **NoMatch** es **False**. Si se produce un error, **NoMatch** es **True** y el registro activo no está definido. En este caso, debe colocar de nuevo el puntero de registros activo en un registro válido.

Usar los métodos **Find** con conjuntos de registros a los que se accede por ODBC con conexión a un motor de base de datos de Microsoft Access puede resultar ineficiente. Tal vez observe que resulta más rápido reformular los criterios para buscar un determinado registro, especialmente al trabajar con conjuntos de registros de gran tamaño.

Al trabajar con grandes objetos **Recordset** de tipo conjunto de registros dinámicos y bases de datos ODBC conectadas a un motor de base de datos de Microsoft Access, puede que compruebe que usar los métodos **Find** o las propiedades **Sort** o **Filter** resulta lento. Para mejorar el rendimiento, use consultas SQL con cláusulas ORDER BY o WHERE personalizadas, consultas de parámetros u objetos **QueryDef** que recuperen registros indexados concretos.

Debe utilizar el formato de fecha de EE.UU. (mes-día-año) cuando busca campos que contienen fechas, incluso si no utiliza la versión americana del motor de base de datos de Microsoft Access; de lo contrario, es posible que no se encuentre la fecha. Utilice la función **Format** de Visual Basic para convertir la fecha. Por ejemplo:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Si criteria está compuesto de una cadena que se concatena con un valor no entero y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice y lngPrice = 125,50), se produce un error al intentar Llame al método. Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.


> [!NOTE]
> - Para obtener el mejor rendimiento, los *criterios* deben tener el formulario "*campo* = *valor*" donde *campo* es un campo indizado en la tabla base subyacente o "*campo* LIKE *prefijo*" donde *campo* es un campo indizado en la tabla base subyacente y *prefijo* es una cadena de búsqueda de prefijo (por ejemplo, "ART *").
> 
> - En general, para tipos de búsquedas equivalentes, el método **Seek** proporciona un mejor rendimiento que los métodos **Find**. Esto supone que los objetos **Recordset** de tipo tabla por sí mismos pueden satisfacer sus necesidades.


## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se muestra cómo usar los métodos FindFirst y FindNext para buscar un registro en un Recordset.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
