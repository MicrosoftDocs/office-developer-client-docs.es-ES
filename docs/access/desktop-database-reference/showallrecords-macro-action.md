---
title: Acción de Macro MostrarTodosRegistros
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b6482bcd34562e13e1783f8e0702718eeaed0b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881737"
---
# <a name="showallrecords-macro-action"></a>Acción de Macro MostrarTodosRegistros


**Se aplica a**: Access 2013, Office 2013


Puede utilizar la acción **MostrarTodosRegistros** para quitar cualquier filtro aplicado de la tabla activa, conjunto de resultados de consulta o formulario y mostrar todos los registros en la tabla o conjunto de resultados o todos los registros en el formulario de la tabla o consulta base.

## <a name="setting"></a>Configuración

La acción **MostrarTodosRegistros** no tiene ningún argumento.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para asegurarse de que se muestran todos los registros (incluidos los registros nuevos o modificados) de una tabla, un conjunto de resultados de consulta o un formulario. Esta acción realiza una nueva consulta de los registros de un formulario o subformulario.

También puede usar esta acción para quitar cualquier filtro que se ha aplicado con la acción **AplicarFiltro** , el comando de **filtro** en la ficha **Inicio** , o el **Nombre del filtro** o el argumento **Condición Where** de la acción **AbrirFormulario** .

Esta acción tiene el mismo efecto que hacer clic en **Alternar filtro** en la ficha **Inicio** , o bien el campo filtrado y haciendo clic en **Quitar filtro de...** en la vista formulario, vista Diseño o vista Hoja de datos.

Para ejecutar la acción **MostrarTodosRegistros** en un módulo Visual Basic para aplicaciones (VBA), use el método **ShowAllRecords** del objeto **DoCmd** .

## <a name="example"></a>Ejemplo

**Aplicar un filtro con una macro**

La siguiente macro contiene un conjunto de acciones, cada una de las cuales filtra los registros para un formulario Lista de teléfonos de clientes. La macro muestra el uso de las acciones **AplicarFiltro**, **MostrarTodosRegistros** e **IrAControl**. También muestra el uso de condiciones para determinar qué botón de alternar en un grupo de opciones se seleccionó en el formulario. Cada fila de acción está asociada con un botón de alternar que selecciona el conjunto de registros que comienzan con A, B, C, y así sucesivamente. Esta macro se debe adjuntar al evento **DespuésDeActualizar** del grupo de opción FiltroNombreCompañía.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condición</p></th>
<th><p>Acción</p></th>
<th><p>Argumentos: Configuración</p></th>
<th><p>Comentario</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Filtros de nombres de compañía] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que comienzan con A, À, Á, Â, Ã o Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombres de compañía] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;B *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen con B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombres de compañía] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[CÇ] *&quot;</p></td>
<td><p>Filtrar por nombres de compañía que empiecen por C o Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Las filas de acciones de la D a la Y tienen el mismo formato que las de la A a la C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombres de compañía] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[ZÆØÅ] *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen por Z, Æ, Ø o Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombres de compañía] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Mostrar todos los registros.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: NombreDeEmpresa</p></td>
<td><p>Si se devuelven registros para la letra seleccionada, mueve el enfoque al control NombreCompañía.</p></td>
</tr>
</tbody>
</table>

