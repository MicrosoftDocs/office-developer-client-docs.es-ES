---
title: EncontrarRegistro (acción de macro)
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 26a0a9fe66fb726bb728872ee31771d12b262864
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923703"
---
# <a name="searchforrecord-macro-action"></a>EncontrarRegistro (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **EncontrarRegistro** para buscar un registro específico en una tabla, una consulta, un formulario o un informe.

## <a name="setting"></a>Configuración

La acción **EncontrarRegistro** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>Especifique o seleccione el tipo de objeto de base de datos en el que desee realizar la búsqueda. Las opciones son <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong> o <strong>Informe</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>Especifique o seleccione el objeto específico que contenga el registro que desee buscar. En la lista desplegable se muestran todos los objetos de base de datos del tipo seleccionado para el argumento <strong>Tipo de objeto</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Registro</strong></p></td>
<td><p>Especifique el punto inicial y la dirección de la búsqueda.</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Anterior</strong></p></td>
<td><p>Permite buscar hacia atrás a partir del actual registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>Siguiente</strong></p></td>
<td><p>Permite buscar hacia delante a partir del actual registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Primero</strong></p></td>
<td><p>Permite buscar hacia delante a partir del primer registro. Es el valor predeterminado de este argumento.</p></td>
</tr>
<tr class="even">
<td><p><strong>Último</strong></p></td>
<td><p>Permite buscar hacia atrás a partir del último registro.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Escriba los criterios para la búsqueda con la misma sintaxis que una cláusula WHERE de SQL, pero sin la palabra &quot;donde&quot;. Por ejemplo,</p>
<p>`Description = "Beverages"`</p>
<p>Para crear un criterio que incluya un valor de un cuadro de texto en un formulario, cree una expresión que concatene la primera parte del criterio con el nombre del cuadro de texto que contenga el valor que desee buscar. Por ejemplo, el siguiente criterio buscará en el campo denominado Descripción el valor del cuadro de texto denominado txtDescripción del formulario denominado frmCategorías. Tenga en cuenta el signo igual (<strong>=</strong>) al principio de la expresión y el uso de comillas simples (<strong>'</strong>) a ambos lados de la referencia del cuadro de texto:</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- En los casos en los que más de un registro coincida con los criterios del argumento **Condición Where**, los siguientes factores determinarán el registro encontrado:
    
  - **El valor del argumento Registro **Vea la tabla que figura en la sección Valor para obtener más información sobre el argumento **Registro**.
    
  - **El criterio de ordenación de los registros **Por ejemplo, si el argumento **Registro** está establecido en **Primero**, un cambio del criterio de ordenación de los registros podría cambiar el registro que se va a encontrar.

- El objeto especificado en el argumento **Nombre del objeto** debe estar abierto antes de que se ejecute esta acción. En caso contrario, se genera un error.

- Si no se cumplen los criterios del argumento **Condición Where**, no se genera ningún error y el foco permanece en el actual registro.

- Cuando se busca el registro anterior o siguiente, la búsqueda no se "ajusta" al alcanzar el final de los datos. Si no hay registros que cumplan los criterios, no se genera ningún error y el foco permanece en el actual registro. Para confirmar que se ha encontrado una coincidencia, se puede especificar una condición para la siguiente acción y equiparar la condición a los criterios del argumento **Condición Where**.

- Para ejecutar la acción **EncontrarRegistro** en un módulo de VBA, use el método **SearchForRecord** del objeto **DoCmd**.

- La acción **EncontrarRegistro** es similar a la acción **[BuscarRegistro](findrecord-macro-action.md)**, pero **EncontrarRegistro** tiene características de búsqueda más eficaces. La acción **BuscarRegistro** se usa principalmente para buscar cadenas y duplica la funcionalidad del cuadro de diálogo **Buscar**. La acción **EncontrarRegistro** usa criterios más similares a las de un filtro o una consulta SQL. En la siguiente lista se muestran algunas de las operaciones que se pueden realizar con la acción **EncontrarRegistro**:
    
  - Se pueden usar criterios complejos en el argumento **Condición Where**, como
        
    `Description = "Beverages" and CategoryID = 11`
    
  - Se puede hacer referencia a campos del origen de registros de un formulario o informe que no se muestran en el formulario o informe. En el ejemplo anterior, ni Description ni CategoryID pueden aparecer en el formulario o informe para que funcionen los criterios.
    
  - Se pueden usar operadores lógicos, como **\<**, **\>**, **Y**, **O** y **ENTRE**. La acción **BuscarRegistro** sólo busca las cadenas que sean iguales, comiencen o contengan la cadena que se está buscando.

## <a name="example"></a>Ejemplo

En la siguiente macro se abre primero la tabla Categorías mediante la acción **AbrirTabla**. A continuación, se usa la acción **EncontrarRegistro** para buscar el primer registro de la tabla donde el campo Descripción sea igual a "Bebidas".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Acción</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>AbrirTabla</strong></p></td>
<td><p><strong>Nombre de la tabla</strong>: categorías<strong>vista</strong>: <strong>Modo DatasheetData</strong>: <strong>Editar</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>EncontrarRegistro</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>Nombre de TableObject</strong>: categorías de<strong>registro</strong>: <strong>Condición de FirstWhere</strong>: descripción = &quot;bebidas&quot;</p></td>
</tr>
</tbody>
</table>

