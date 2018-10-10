---
title: CambiarNombreDeObjeto (acción de macro)
TOCTitle: RenameObject Macro Action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6522e85aa0407800ea0aade039a65c79a25c1419
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484386"
---
# <a name="renameobject-macro-action"></a>CambiarNombreDeObjeto (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

Puede usar la acción **CambiarNombreDeObjeto** para cambiar el nombre de un objeto de base de datos especificado.


> [!NOTE]
> <P>[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</P>



## <a name="setting"></a>Configuración

La acción **CambiarNombreDeObjeto** tiene los siguientes argumentos.

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

</p>

> [!NOTE]
> <P>Si ejecuta una macro que contiene la acción <STRONG>CambiarNombre</STRONG> en una base de datos de biblioteca, Microsoft Access primero busca el objeto con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El nuevo nombre del objeto de base de datos debe cumplir las convenciones de nomenclatura estándar para los objetos de Access.

No se puede cambiar el nombre de un objeto abierto.

Si se dejan en blanco los argumentos **Tipo de objeto** y **Nombre anterior**, Access cambia el nombre del objeto seleccionado en el panel de navegación. Para seleccionar un objeto en el panel de navegación, se puede utilizar la acción **SeleccionarObjeto** con el valor del argumento** En panel de navegación** establecido en **Sí**.

Para cambiar el nombre de un objeto, también se puede hacer clic con el botón secundario en dicho botón en el panel de navegación, hacer clic en **Cambiar nombre** y escribir un nombre nuevo. Con la acción **CambiarNombreDeObjeto**, no es preciso seleccionar primero el objeto en el panel de navegación y tampoco hay que detener la macro para escribir el nuevo nombre.

Esta acción se diferencia de la acción **CopiarObjeto**, con la que se crea una copia del objeto con un nombre nuevo.

Para ejecutar la acción **CambiarNombreDeObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Rename** del objeto **DoCmd**.

