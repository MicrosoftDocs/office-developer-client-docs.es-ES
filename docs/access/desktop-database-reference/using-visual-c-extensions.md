---
title: Utilizar Extensiones de Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcfde7e343a37d65356e1f9ed8d879030913f5ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868787"
---
# <a name="using-visual-c-extensions"></a>Utilizar Extensiones de Visual C++


**Se aplica a**: Access 2013, Office 2013

## <a name="the-iadorecordbinding-interface"></a>Interfaz IADORecordBinding

Las Extensiones de Microsoft Visual C++ para ADO asocian o enlazan los campos de un objeto [Recordset](recordset-object-ado.md) a las variables de C/C++. Cuando cambia la actual fila del objeto **Recordset** enlazado, todos los campos enlazados del objeto **Recordset** se copian en las variables de C/C++. Si es necesario, los datos copiados se convierten en el tipo de datos declarado de la variable de C/C++.

El método **BindToRecordset** de la interfaz **IADORecordBinding** asocia los campos a las variables de C/C++. El método **AddNew** agrega una fila nueva al objeto **Recordset** enlazado. El método **Update** rellena los campos en las nuevas filas del objeto **Recordset** o actualiza los campos en las filas existentes con el valor de las variables de C/C++.

La interfaz **IADORecordBinding** la implementa el objeto **Recordset**. La implementación no se realiza mediante código del usuario.

## <a name="binding-entries"></a>Entradas de enlace

Las Extensiones de Visual C++ para ADO asignan los campos de un objeto [Recordset](recordset-object-ado.md) a las variables de C/C++. La definición de una asignación entre un campo y una variable se denomina *entrada de enlace*. Las macros proporcionan entradas de enlace para los datos numéricos, datos de longitud fija y de longitud variable. Las entradas de enlace y las variables de C/C++ se declaran en una clase derivada de la clase **CADORecordBinding** de Extensiones de Visual C++. La clase **CADORecordBinding** la definen internamente las macros de entradas de enlace.

ADO asigna internamente los parámetros de estas macros a una estructura **DBBINDING** de OLE DB y crea un objeto **Accessor** de OLE DB para administrar el movimiento y la conversión de los datos entre los campos y las variables. OLE DB define los datos como datos que se componen de tres partes: un *búfer* donde se almacenan los datos, un *estado* que indica si un campo se ha almacenado correctamente en el búfer o cómo debe restaurarse la variable en el campo, y la *longitud* de los datos. (Si desea obtener más información, vea el Capítulo 6 de *Referencia del programador de OLE DB*: Obtener y establecer datos.)

## <a name="header-file"></a>Archivo de encabezado

Incluya el archivo siguiente en la aplicación para que pueda utilizar las Extensiones de Visual C++ para ADO:

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Enlazar campos del objeto Recordset

**Para enlazar campos del objeto Recordset a las variables de C/C++**

1.  Cree una clase derivada de la clase **CADORecordBinding**.

2.  Especifique las entradas de enlace y las correspondientes variables de C/C++ en la clase derivada. Inserte las entradas de enlace entre **comenzar\_ADO\_enlace** y **END\_ADO\_enlace** las macros. No termine las macros con comas ni signos de punto y coma. Cada macro especifica automáticamente los delimitadores apropiados. Especifique una entrada de enlace por cada campo que se va a asignar a una variable de C/C++. Utilice un miembro apropiado de la **ADO\_fijo\_longitud\_entrada**, **ADO\_numérico\_entrada**, o **ADO\_VARIABLE\_longitud\_entrada** familia de macros.

3.  En la aplicación, cree una instancia de la clase derivada de **CADORecordBinding**. Obtenga la interfaz **IADORecordBinding** del objeto **Recordset**. A continuación, llame al método **BindToRecordset** para asociar los campos del objeto **Recordset** a las variables de C/C++.

Vea [Ejemplo de Extensiones de Visual C++](visual-c-extensions-example.md) para obtener más información.

## <a name="interface-methods"></a>Métodos de interfaz

La interfaz **IADORecordBinding** tiene tres métodos: **BindToRecordset**, **AddNew** y **Update**. El único argumento de cada método es un puntero a una instancia de la clase derivada de **CADORecordBinding**. Por lo tanto, los métodos **AddNew** y **Update** no pueden especificar ninguno de los parámetros de los homónimos de ADO de sus métodos.

**Sintaxis**

El método **BindToRecordset** asocia los campos del objeto **Recordset** a las variables de C/C++.

`BindToRecordset(CADORecordBinding *binding)` 

El método **AddNew** invoca su homónimo, el método [AddNew](addnew-method-ado.md) de ADO, para agregar una fila nueva al objeto **Recordset**.

`AddNew(CADORecordBinding *binding)` 

El método **Update** invoca su homónimo, el método [Update](update-method-ado.md) de ADO, para actualizar el objeto **Recordset**.

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Macros de entradas de enlace

Las macros de entradas de enlace definen la asociación de un campo del objeto **Recordset** y una variable. Una macro inicial y una macro final delimitan el conjunto de entradas de enlace.

Hay familias de macros para datos de longitud fija, como **adDate** o **adBoolean**, datos numéricos como **adTinyInt**, **adInteger** o **adDouble**, y datos de longitud variable como **adChar**, **adVarChar** o **adVarBinary**. Todos los tipos numéricos, excepto **adVarNumeric**, son también tipos de longitud fija. Cada familia tiene diferentes conjuntos de parámetros de modo que se puede excluir la información de enlace que no sea de interés.

Vea los tipos de datos de *referencia del programador de OLE DB,* Apéndice A: para obtener información adicional.

_**Comenzar entradas de enlace**_

**COMENZAR\_ADO\_enlace**(*clase*)

_**Datos de longitud fija**_

**ADO\_fijo\_longitud\_entrada**(*Ordinal, el tipo de datos, el búfer, el estado, modificar*)  
**ADO\_fijo\_longitud\_ENTRY2**(*Ordinal, el tipo de datos, el búfer, modificar*)

_**Datos numéricos**_

**ADO\_numérico\_entrada**(*Ordinal, tipo de datos, búfer, precisión, escala, estado, modificar*)  
**ADO\_numérico\_ENTRY2**(*Ordinal, tipo de datos, búfer, precisión, escala, modificar*)

_**Datos de longitud variable**_

**ADO\_VARIABLE\_longitud\_entrada**(*Ordinal, tipo de datos, búfer, tamaño, estado, longitud, modificar*)  
**ADO\_VARIABLE\_longitud\_ENTRY2**(*Ordinal, tipo de datos, búfer, tamaño, estado, modificar*)  
**ADO\_VARIABLE\_longitud\_Entrada3**(*Ordinal, tipo de datos, búfer, tamaño, longitud, modificar*)  
**ADO\_VARIABLE\_longitud\_Entrada4**(*Ordinal, el tipo de datos, el búfer, el tamaño, modificar*)

_**End entradas de enlace**_

**END\_ADO\_enlace** ()

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Class</em></p></td>
<td><p>Clase en la que se definen las entradas de enlace y las variables de C/C++.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Número ordinal, a partir de 1, del campo del objeto <strong>Recordset</strong> correspondiente a la variable de C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Tipo de datos de ADO equivalente de la variable de C/C++ (vea <a href="datatypeenum.md">DataTypeEnum</a> para obtener una lista de tipos de datos válidos). El valor del campo del objeto <strong>Recordset</strong> se convertirá en este tipo de datos si es necesario.</p></td>
</tr>
<tr class="even">
<td><p><em>Buffer</em></p></td>
<td><p>Nombre de la variable de C/C++ donde se almacenará el campo del objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Tamaño máximo, en bytes, de <em>Buffer</em>. Si <em>Buffer</em> va a contener una cadena de longitud variable, deje espacio para un cero final.</p></td>
</tr>
<tr class="even">
<td><p><em>Status</em></p></td>
<td><p>Nombre de una variable que va a indicar si el contenido de <em>Buffer</em> es válido y si la conversión del campo en <em>DataType</em> se ha realizado correctamente.
 Los dos valores más importantes de esta variable son <strong>adFldOK</strong> y <strong>adFldNull</strong>, es decir, la conversión se ha realizado correctamente y el valor del campo es VARIANT de tipo VT_NULL y no está vacío, respectivamente. Los posibles valores de <em>estado</em> se enumeran en la tabla siguiente, &quot;valores de estado.&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modificar</em></p></td>
<td><p>Marca de operador booleano. Si su valor es TRUE, indica que ADO puede actualizar el correspondiente campo de <strong>Recordset</strong> con el valor de <em>Buffer</em>.
 Establezca el valor del parámetro booleano <em>Modify</em> en TRUE para que ADO pueda actualizar el campo enlazado. Establézcalo en FALSE si desea examinar el campo sin cambiarlo.</p></td>
</tr>
<tr class="even">
<td><p><em>Precision</em></p></td>
<td><p>Número de dígitos que se pueden representar en una variable numérica.</p></td>
</tr>
<tr class="odd">
<td><p><em>Scale</em></p></td>
<td><p>Número de posiciones de decimales en una variable numérica.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Nombre de una variable de cuatro bytes que va a contener la longitud real de los datos en <em>Buffer</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Valores de Status

El valor de la variable *Status* indica si un campo se ha copiado correctamente a una variable.

Al configurar los datos, puede que el valor de *Status* sea **adFldNull** para indicar que el campo del objeto **Recordset** debe establecerse en null.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Se ha devuelto un valor de campo que no sea null.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1</p></td>
<td><p>El enlace no es válido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>El valor no se ha podido convertir por motivos que no sean la falta de coincidencia de los signos o el desbordamiento de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3</p></td>
<td><p>Al obtener un campo, indica que se ha devuelto un valor null.
 Cuando establece un campo, indica que el campo debe establecerse en <strong>NULL</strong> cuando no puede codificar <strong>NULL</strong> por sí mismo (por ejemplo, una matriz de caracteres o un entero).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Se han truncado los datos de longitud variable o los dígitos numéricos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>El valor tiene signo y el tipo de datos no lo tiene.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldDataOverFlow</strong></p></td>
<td><p>6</p></td>
<td><p>El valor es mayor que el valor que se puede almacenar en el tipo de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>El campo y el tipo de columna desconocidos ya están abiertos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>No se ha podido determinar el valor del campo. Por ejemplo, en un nuevo campo no asignado sin valor predeterminado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Al actualizar, no hay permiso para escribir datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Al actualizar, el valor de campo infringirá la integridad de las columnas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Al actualizar, el valor de campo infringirá el esquema de las columnas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Al actualizar, parámetro de estado no válido.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Al actualizar, se ha utilizado un valor predeterminado.</p></td>
</tr>
</tbody>
</table>

