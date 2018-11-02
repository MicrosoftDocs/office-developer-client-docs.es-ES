---
title: EliminarObjeto (acción de macro)
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 65072fcc418e6a75ea1684c6830f3acfc4875aee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921946"
---
# <a name="deleteobject-macro-action"></a>EliminarObjeto (acción de macro)


**Se aplica a**: Access 2013, Office 2013

La acción **EliminarObjeto** permite eliminar un objeto de base de datos especificado.


> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.

## <a name="setting"></a>Configuración

La acción **EliminarObjeto** tiene los argumentos siguientes.

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
<td><p>Tipo de objeto que se va a eliminar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong>, en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Para eliminar el objeto seleccionado en el panel de navegación, deje este argumento en blanco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>El nombre del objeto que se va a eliminar. El cuadro <strong>Nombre de objeto</strong> muestra todos los objetos de la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el cuadro <strong>Tipo de objeto</strong> , deje también en blanco este cuadro. Si ejecuta una macro que contenga la acción <strong>EliminarObjeto</strong> en una base de datos de biblioteca, Microsoft Office Access 2007 busca primero el objeto con este nombre en la base de datos de biblioteca y, después, en la base de datos activa.</p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> [!PRECAUCIóN] Si deja en blanco los cuadros **Tipo de objeto** y **Nombre del objeto**, Access elimina el objeto seleccionado en el panel de navegación sin mostrar ningún mensaje de advertencia cuando encuentra la acción **EliminarObjeto**.



## <a name="remarks"></a>Comentarios

Puede usar la acción **EliminarObjeto** para eliminar objetos temporales creados mientras se ejecutaba la macro. Por ejemplo, podría utilizar la acción **AbrirConsulta** para ejecutar una consulta de creación de tabla que cree una tabla temporal. Cuando termine de usar la tabla temporal, puede ejecutar la acción **EliminarObjeto** para eliminarla.

Esta acción tiene el mismo efecto que seleccionar un objeto en el panel de navegación y presionar la tecla SUPR o hacer clic con el botón secundario en el objeto del panel de navegación y seleccionar **Eliminar**.

Para ejecutar la acción **EliminarObjeto** en un módulo de Visual Basic para Aplicaciones, puede usar el método **DeleteObject** del objeto **DoCmd**.

