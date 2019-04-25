---
title: Método Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300640"
---
# <a name="recordsetfindnext-method-dao"></a>Método Recordset.FindNext (DAO)

**Se aplica a:** Access 2013, Office 2013

Localiza el registro siguiente de un objeto **[Recordset](recordset-object-dao.md)** de tipo dynaset o de tipo snapshot que satisface los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expression* .FindNext(***Criteria***)

*expression* Variable que representa un objeto **Recordset**.

## <a name="parameters"></a>Parameters

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
<td><p><em>Criterios</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Cadena que se utiliza para localizar el registro. Es como una cláusula WHERE en una instrucción SQL pero sin la palabra WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

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

Usar los métodos **Find** con conjuntos de registros a los que se accede por ODBC con conexión a un motor de base de datos de Microsoft Access puede resultar ineficiente. Tal vez observe que resulta más rápido reformular los criterios para buscar un determinado registro, especialmente al trabajar con conjuntos de registros de gran tamaño.

En un área de trabajo de ODBCDirect, los métodos **Find** y **Seek** no están disponibles en todo tipo de objetos **Recordset** porque no es muy eficaz ejecutar **Find** o **Seek** mediante una conexión ODBC a través de la red. En su lugar, debe diseñar la consulta (es decir, usar el argumento source en el método **OpenRecordset**) con una cláusula WHERE adecuada que limite los registros devueltos a solo aquellos que cumplen los criterios que use en un método **Find** o **Seek**.

Al trabajar con bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access y objetos de tipo dynaset grandes, es posible que vea que el uso de métodos **Find** o de la propiedad **Sort** o **Filter** es lento. Para mejorar el rendimiento, utilice las consultas SQL con cláusulas ORDER BY o WHERE personalizadas, consultas de parámetros u objetos **QueryDef** que recuperan registros indizados específicos.

Al buscar en campos que contengan fechas, debe usar el formato de fecha estadounidense (mes-día-año), aunque no esté usando la versión estadounidense del motor de base de datos de Microsoft Access. Si no lo hace así, es posible que no encuentre los datos. Use la función de Visual Basic **Format** para convertir la fecha. Por ejemplo:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Si criteria está compuesto por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU. como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), se produce un error cuando intenta llamar al método. Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.

> [!NOTE]
> - Para obtener el mejor rendimiento, los *criterios* deben tener la forma "*campo* = *valor*" donde *campo* es un campo indexado de la tabla base subyacente, o "*campo* LIKE *prefijo*" donde *campo* es un campo indexado de la tabla base subyacente y *prefijo* es una cadena de búsqueda de prefijo (por ejemplo, "ART*").
> 
> - En general, con tipos de búsquedas equivalentes, el método **Seek** proporciona mejor rendimiento que los métodos **Find**, siempre que no necesite más que los objetos **Recordset** de tipo tabla por sí solos.


## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se muestra cómo usar los métodos FindFirst y FindNext para buscar un registro en un Recordset.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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
