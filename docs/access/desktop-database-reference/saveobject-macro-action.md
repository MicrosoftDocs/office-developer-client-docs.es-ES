---
title: GuardarObjeto (acción de macro)
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308935"
---
# <a name="saveobject-macro-action"></a>GuardarObjeto (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **GuardarObjeto** para guardar el objeto de Access especificado o el objeto activo si ninguno está especificado. También puede guardar el objeto activo con un nombre nuevo en algunos casos (esto funciona de la misma forma que el comando **Guardar como** en la **Barra de herramientas de acceso rápido**).

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **GuardarObjeto** tiene los siguientes argumentos.

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
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>El tipo de objeto que desea guardar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> en la sección <strong>Argumentos de acción</strong> del panel del Generador de macros. Para seleccionar el objeto activo, deje este argumento en blanco. Si selecciona un tipo de objeto en este argumento, debe seleccionar el nombre de un objeto existente en el argumento <strong>Nombre de objeto</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>El nombre del objeto que desea guardar. El cuadro <strong>Nombre de objeto</strong> muestra todos los objetos en la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja el argumento <strong>Tipo de objeto</strong> en blanco, puede dejar este argumento en blanco para guardar el objeto activo o, en algunos casos, escribir un nombre nuevo en este argumento para guardar el objeto activo con este nombre. Si escribe un nombre nuevo, el nombre debe cumplir con las convenciones de denominación estándar para objetos de Microsoft Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **GuardarObjeto** funciona en todos los objetos de base de datos que el usuario puede abrir explícitamente y guardar. El objeto especificado se debe abrir para la acción **GuardarObjeto** para que tenga efecto en el objeto. Esta acción tiene el mismo efecto que seleccionar un objeto y guardarlo al hacer clic en **Guardar** en la **Barra de herramientas de acceso rápido**. 

Dejar el argumento **Tipo de objeto** en blanco y escribir un nombre nuevo en el argumento **Nombre de objeto** tiene el mismo efecto que hacer clic en **Guardar como** en la **Barra de herramientas de acceso rápido**, y escribir un nombre nuevo para el objeto activo. Con la acción **GuardarObjeto** puede especificar un objeto para guardar y ejecutar un comando **Guardar como** desde una macro.

> [!NOTE]
> No puede utilizar la acción **GuardarObjeto** para guardar cualquiera de los siguientes con un nombre nuevo:
> - Un formulario en la vista Formulario o en la vista Hoja de datos
> - Un informe en vista previa de impresión
> - Un módulo
> - Vista de servidor en vista Hoja de datos o Vista previa de impresión
> - Una página de acceso a datos en la vista Página
> - Una tabla en la vista Hoja de datos o vista previa de impresión
> - Una consulta en la vista Hoja de datos o vista previa de impresión
> - Procedimiento almacenado en la vista Hoja de datos o vista previa de impresión

La acción **GuardarObjeto**, si se lleva a cabo en una macro que se ejecuta en la base de datos activa o en una base de datos de biblioteca, siempre guarda el objeto especificado en la base de datos en la que se creó el objeto.

Si guarda el objeto activo con un nombre nuevo, pero el nombre es el mismo que el de un objeto existente de este tipo, un cuadro de diálogo solicita si desea sobrescribir el objeto existente. Si estableció el argumento **Activar advertencias** de la acción **EstablecerAdvertencias** como **No**, el cuadro de diálogo no se muestra y el objeto antiguo se sobrescribe automáticamente.

Para ejecutar la acción **GuardarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **Save** del objeto **DoCmd**.

