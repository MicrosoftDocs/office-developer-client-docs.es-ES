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


Puede usar la acción **ShowAllRecords** para quitar cualquier filtro aplicado de la tabla activa, conjunto de resultados de consulta o formulario, y mostrar todos los registros de la tabla o conjunto de resultados o todos los registros de la tabla o consulta subyacentes del formulario.

## <a name="setting"></a>Setting

La **acción ShowAllRecords** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para asegurarse de que todos los registros (incluidos los registros nuevos o modificados) se muestran para una tabla, conjunto de resultados de consulta o formulario. Esta acción provoca una nueva consulta de los registros de un formulario o subformulario.

También puede usar esta acción para quitar cualquier filtro que  se aplicó con la  acción **AplicarFiltro,** el comando Filtro de la ficha Inicio o el argumento Nombre de filtro o Condición Where de la acción   **AbrirFormulario.**

Esta acción tiene el  mismo efecto  que hacer clic en Alternar filtro en la ficha Inicio o hacer clic con el botón secundario en el campo filtrado y hacer clic en Borrar filtro **desde...** en la vista Formulario, vista Diseño o Vista Hoja de datos.

Para ejecutar la **acción ShowAllRecords** en un módulo Visual Basic para Aplicaciones (VBA), utilice el método **ShowAllRecords** del **objeto DoCmd.**

## <a name="example"></a>Ejemplo

**Aplicar un filtro mediante una macro**

La macro siguiente contiene un conjunto de acciones, cada una de las cuales filtra los registros de un formulario Lista de teléfonos de clientes. Muestra el uso de las acciones **ApplyFilter**, **ShowAllRecords** y **GoToControl.** También muestra el uso de condiciones para determinar qué botón de alternancia de un grupo de opciones se ha seleccionado en el formulario. Cada fila de acción está asociada con un botón de alternancia que selecciona el conjunto de registros a partir de A, B, C, y así sucesivamente, o todos los registros. Esta macro debe adjuntarse al **evento AfterUpdate** del grupo de opciones CompanyNameFilter.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Acción</p></th>
<th><p>Argumentos: Configuración</p></th>
<th><p>Comentario</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Filtros de nombre de empresa] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [Company Name] Like &quot; [AÀÁÂÃÄ]*&quot;</p></td>
<td><p>Filtra por nombres de compañía que comienzan por A, À, Á, Â, Ã o Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombre de empresa] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [Nombre de la compañía] Como &quot; B*&quot;</p></td>
<td><p>Filtra por los nombres de compañía que comienzan por B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombre de empresa] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [Company Name] Like &quot; [CÇ]*&quot;</p></td>
<td><p>Filtra por los nombres de compañía que comienzan por C o Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Las filas de acción de D a Y tienen el mismo formato que A a C...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nombre de empresa] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condición Where</strong>: [Company Name] Like &quot; [ZÆØÅ]*&quot;</p></td>
<td><p>Filtra por los nombres de compañía que comienzan por Z, Æ, Ø o Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nombre de empresa] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Mostrar todos los registros.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt; 0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: NombreDeEmpresa</p></td>
<td><p>Si se devuelven registros para la letra seleccionada, mueva el foco al control CompanyName.</p></td>
</tr>
</tbody>
</table>

