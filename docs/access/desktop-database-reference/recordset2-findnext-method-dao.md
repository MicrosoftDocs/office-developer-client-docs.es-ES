---
title: Método Recordset2. FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: dc1d9fdf-36ae-cb23-4949-f7b98cb5d4e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835354(v=office.15)
ms:contentKeyID: 48548121
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5526c571e53021c1b27aad8f3c18d7ebdc9ecb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309431"
---
# <a name="recordset2findnext-method-dao"></a>Método Recordset2. FindNext (DAO)

**Se aplica a:** Access 2013, Office 2013

Localiza el registro siguiente de un objeto **[Recordset](recordset-object-dao.md)** de tipo dynaset o de tipo snapshot que satisface los criterios especificados y hace que el registro sea el registro activo (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . FindNext (***criterios***)

*expresión* Variable que representa un objeto **Recordset2** .

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
<td><p><em>Criteria</em></p></td>
<td><p>Obligatorio</p></td>
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
<th><p>Iniciar la búsqueda en</p></th>
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
<td><p>Fin del conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Registro actual</p></td>
<td><p>Inicio del conjunto de registros</p></td>
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

Si Criteria está compuesto por una cadena concatenada con un valor que no sea entero, y los parámetros del sistema especifican un carácter no. decimal como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice e lngPrice = 125, 50), se producirá un error cuando intente llamar al método. Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.

> [!NOTE]
> - Para un mejor rendimiento, los *criterios** deben tener el formato "*valor*de*campo* = " donde *campo* es un campo indizado en la tabla base subyacente o "*campo* like prefijo" donde ** *campo* es un un campo indizado en la tabla base ** subyacente y prefijo es una cadena de búsqueda de prefijo (por ejemplo, "Art *").
> - En general, para tipos de búsquedas equivalentes, el método **Seek** proporciona un mejor rendimiento que los métodos **Find**. Esto supone que los objetos **Recordset** de tipo tabla por sí mismos pueden satisfacer sus necesidades.


