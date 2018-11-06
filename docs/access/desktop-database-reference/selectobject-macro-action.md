---
title: SeleccionarObjeto (acción de macro)
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b34deff80157b3de63038251a649794587dacc85
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997416"
---
# <a name="selectobject-macro-action"></a>SeleccionarObjeto (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **SeleccionarObjeto** para seleccionar un determinado objeto de base de datos.

## <a name="setting"></a>Configuración

La acción **SeleccionarObjeto** utiliza los siguientes argumentos.

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
<td><p>El tipo de objeto de base de datos que se desea seleccionar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Páginas de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>Nombre del objeto que se va a seleccionar. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong> que existen en la base de datos. Este argumento es obligatorio, a menos que el argumento En panel de navegación se haya establecido en <strong>Sí</strong>.</p><p><strong>Nota</strong>: los nombres de objeto para objetos <STRONG>Vista de servidor</STRONG>, <STRONG>diagrama</STRONG>o <STRONG>Procedimiento almacenado</STRONG> no se muestran en el cuadro <STRONG>Nombre de objeto</STRONG> de un proyecto de Access (.adp).</p></td>
</tr>
<tr class="odd">
<td><p><strong>En panel de navegación</strong></p></td>
<td><p>Especifica si Microsoft Access selecciona el objeto en el Panel de navegación. Haga clic en <strong>Sí</strong> (para seleccionar el objeto en el Panel de navegación) o <strong>No</strong> (para no seleccionar el objeto en el Panel de navegación). El valor predeterminado es <strong>No</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **SeleccionarObjeto** funciona con cualquier objeto de Access capaz de recibir el enfoque. Esta acción aplica el enfoque al objeto especificado y lo muestra si está oculto. Si el objeto es un formulario, la acción **SeleccionarObjeto** establece la propiedad **Visible** del formulario en **Sí** y devuelve el formulario al modo establecido por las propiedades del formulario (por ejemplo, como formulario modal o formulario emergente).

Si el objeto no está abierto en ninguna de las otras ventanas de Access, se puede seleccionar en el panel de navegación estableciendo previamente el argumento **En panel de navegación** en **Sí**. Si establece el argumento **En panel de navegación** en **No**, aparecerá un mensaje de error cuando intente seleccionar un objeto que no esté abierto.

Puede usar esta acción para seleccionar un objeto sobre el que desee ejecutar acciones adicionales. Por ejemplo, si Access está configurado de modo que use ventanas que se superponen en lugar de documentos con fichas, es posible restaurar un objeto minimizado (mediante la acción **RestaurarVentana** ) o maximizar una ventana que contiene un objeto con el que se desea trabajar (mediante la acción **MaximizarVentana** ).

Si selecciona un formulario, puede utilizar las acciones **IrAControl**, **IrARegistro** e **IrAPágina** para desplazarse a determinadas áreas del formulario. La acción **IrARegistro** también funciona para hojas de datos.

Para ejecutar la acción **SeleccionarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SelectObject** del objeto **DoCmd**.

