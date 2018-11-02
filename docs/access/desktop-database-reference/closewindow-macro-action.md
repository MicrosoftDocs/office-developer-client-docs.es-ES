---
title: CerrarVentana (acción de macro)
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f9bffbd129d8fb4fc1334dbd884556d98e7f140c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929324"
---
# <a name="closewindow-macro-action"></a>CerrarVentana (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **Cerrarventana** para cerrar una ficha de documento de acceso especificada o en la ficha del documento activo si no se especifica ninguno.

## <a name="setting"></a>Configuración

La acción **CerrarVentana** tiene los siguientes argumentos.

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
<td><p>Tipo de objeto cuya ficha de documentos se desea cerrar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong>, en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Para seleccionar la ficha de documentos activa, deje este argumento en blanco. 

</p>

> [!NOTE]
> Si desea cerrar un módulo en el Editor de Visual Basic, debe usar **Módulo** en el argumento **Tipo de objeto**.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>Nombre del objeto que se va a cerrar. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos de la base de datos que tienen el tipo seleccionado en el argumento <strong>Tipo de objeto</strong>. Haga clic en el objeto que desea cerrar. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, también deberá dejar en blanco este argumento.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Indica si deben guardarse los cambios realizados en el objeto cuando se cierre. Haga clic en <strong>Sí</strong> (guardar el objeto), <strong>No</strong> (cerrar el objeto sin guardarlo) o <strong>Preguntar</strong> (preguntar al usuario si desea guardar o no el objeto). El valor predeterminado es <strong>Preguntar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **CerrarVentana** funciona en todos los objetos de base de datos que el usuario puede abrir o cerrar explícitamente. Esta acción tiene el mismo efecto que seleccionar un objeto y después cerrarlo haciendo clic con el botón secundario en la ficha de documentos del objeto y, a continuación, haciendo clic en **Cerrar** en el menú contextual, o hacer clic en el botón **Cerrar** del objeto.

Si el argumento **Guardar** se establece en **Preguntar** y el objeto todavía no se ha guardado antes de ejecutarse la acción **CerrarVentana**, un cuadro de diálogo pedirá al usuario que guarde el objeto antes de que la macro lo cierre. Si se ha establecido el argumento **Activar advertencias** de la acción **EstablecerAdvertencias** en **No**, el cuadro de diálogo no aparece y el objeto se guarda automáticamente.

Para ejecutar la acción **CerrarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **CerrarVentana** del objeto **DoCmd**.

