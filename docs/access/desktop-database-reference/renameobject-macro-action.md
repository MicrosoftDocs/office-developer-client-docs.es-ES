---
title: CambiarNombreDeObjeto (acción de macro)
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306723"
---
# <a name="renameobject-macro-action"></a>CambiarNombreDeObjeto (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **CambiarNombreDeObjeto** para cambiar el nombre de un objeto de base de datos especificado.

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza.

## <a name="setting"></a>Configuración

La acción **CambiarNombreDeObjeto** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nombre nuevo</strong></p></td>
<td><p>Nombre nuevo del objeto de la base de datos. Escriba el nombre del objeto en el cuadro <strong>Nombre nuevo</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Éste es un argumento requerido.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>Tipo del objeto cuyo nombre se desea cambiar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong>. Para cambiar el nombre del objeto seleccionado en el panel de navegación, deje este argumento en blanco.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre anterior</strong></p></td>
<td><p>Nombre del objeto cuyo nombre se va a cambiar. En el cuadro <strong>Nombre anterior</strong> se muestran todos los objetos de la base de datos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento. 

</p><p><strong>NOTA:</strong>Si ejecuta una macro <STRONG></STRONG> que contiene la acción Cambiar nombre en una base de datos de biblioteca, Microsoft Access primero busca el objeto con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El nuevo nombre del objeto de base de datos debe cumplir las convenciones de nomenclatura estándar para los objetos de Access.

No se puede cambiar el nombre de un objeto abierto.

If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.

Para cambiar el nombre de un objeto, también se puede hacer clic con el botón secundario en dicho botón en el panel de navegación, hacer clic en **Cambiar nombre** y escribir un nombre nuevo. Con la acción **CambiarNombreDeObjeto**, no es preciso seleccionar primero el objeto en el panel de navegación y tampoco hay que detener la macro para escribir el nuevo nombre.

Esta acción se diferencia de la acción **CopiarObjeto**, con la que se crea una copia del objeto con un nombre nuevo.

Para ejecutar la acción **CambiarNombreDeObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Rename** del objeto **DoCmd**.

