---
title: MostrarTodosRegistros (acción de macro)
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308648"
---
# <a name="showallrecords-macro-action"></a>MostrarTodosRegistros (acción de macro)


**Se aplica a:** Access 2013, Office 2013


Puede usar la acción **MostrarTodosRegistros** para quitar cualquier filtro aplicado de la tabla activa, el conjunto de resultados de la consulta o el formulario, y Mostrar todos los registros de la tabla o el conjunto de resultados o todos los registros de la tabla o consulta subyacente del formulario.

## <a name="setting"></a>Configuración

La acción **MostrarTodosRegistros** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para asegurarse de que todos los registros (incluidos los registros nuevos o modificados) se muestran para una tabla, un conjunto de resultados de una consulta o un formulario. Esta acción produce una nueva consulta de los registros de un formulario o subformulario.

También puede usar esta acción para quitar cualquier filtro que se haya aplicado con la acción **AplicarFiltro** , el comando **filtrar** en la ficha **Inicio** o el argumento **nombre del filtro** o **Condición Where** de la acción **AbrirFormulario** .

Esta acción tiene el mismo efecto que hacer clic en **alternar filtro** en la ficha **Inicio** o hacer clic con el botón secundario en el campo filtrado y hacer clic en **Borrar filtro de...** en la vista formulario, vista Diseño o vista Hoja de información.

Para ejecutar la acción **MostrarTodosRegistros** en un módulo de Visual Basic para aplicaciones (VBA), use el método **ShowAllRecords** del objeto **DoCmd** .

## <a name="example"></a>Ejemplo

**Aplicar un filtro con una macro**

La siguiente macro contiene un conjunto de acciones, cada una de las cuales filtra los registros de un formulario de lista de teléfonos de clientes. Muestra el uso de las acciones **AplicarFiltro**, **MostrarTodosRegistros**e **IrAControl** . También muestra el uso de condiciones para determinar qué botón de alternancia de un grupo de opciones se ha seleccionado en el formulario. Cada fila de acción se asocia a un botón de alternancia que selecciona el conjunto de registros que comienzan con A, B, C, etc. o todos los registros. Esta macro se debe adjuntar al evento **AfterUpdate** del grupo de opciones CompanyNameFilter.

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
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Filtros de nombre de la compañía] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen por A, À, Á, Â, Ã o Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombre de compañía] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [nombre de la compañía &quot;] like B *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen por B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombre de la compañía] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [cç] *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen por C o Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Las filas de acción de la D a la Y tienen el mismo formato que a hasta C...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombre de compañía] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [ZÆØÅ] *&quot;</p></td>
<td><p>Filtrar por nombres de compañías que empiecen por Z, Æ, Ø o Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombre de la compañía] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Mostrar todos los registros.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. RecordCount &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: NombreDeEmpresa</p></td>
<td><p>Si se devuelven registros para la carta seleccionada, desplace el foco al control CompanyName.</p></td>
</tr>
</tbody>
</table>

