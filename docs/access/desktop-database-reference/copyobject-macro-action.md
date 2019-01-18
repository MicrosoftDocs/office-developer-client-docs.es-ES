---
title: CopiarObjeto (acción de macro)
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d1fb13d04691b7bf5e0aafcc484cfc4f471e1e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715889"
---
# <a name="copyobject-macro-action"></a>CopiarObjeto (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **CopiarObjeto** para copiar el objeto de base de datos especificado a una base de datos de Access diferente o a la misma base de datos o proyecto de Access con un nuevo nombre. Por ejemplo, puede copiar o hacer una copia de seguridad de un objeto existente en otra base de datos o crear rápidamente un objeto similar con algunos cambios.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **CopiarObjeto** tiene los siguientes argumentos.

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
<td><p><strong>Base de datos de destino</strong></p></td>
<td><p>Ruta de acceso y nombre de archivo válidos para la base de datos de destino. Escriba la ruta de acceso y el nombre de archivo en el cuadro <strong>Base de datos de destino</strong>, en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Deje este argumento en blanco si desea seleccionar la base de datos actual. 

</p><p><strong>Nota</strong>: este argumento sólo está disponible en el entorno de base de datos de Access. Cuando se usa esta acción en un entorno de proyecto de Access (.adp), el argumento de base de datos de destino debe estar en blanco.</p>
<p>Si se ejecuta una macro que contiene la acción <strong>CopiarObjeto</strong> en una base de datos de biblioteca y se deja este argumento en blanco, Microsoft Office Access 2007 copiará el objeto a la base de datos de biblioteca.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre nuevo</strong></p></td>
<td><p>Nombre nuevo del objeto. Cuando copie a una base de datos diferente, deje este argumento en blanco si desea mantener el mismo nombre.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo de objeto de origen</strong></p></td>
<td><p>El tipo de objeto que desea copiar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong>. Para copiar el objeto seleccionado en el Panel de navegación, deje este argumento en blanco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de objeto de origen</strong></p></td>
<td><p>El nombre del objeto que se va a copiar. El cuadro <strong>Nombre del objeto de origen</strong> muestra todos los objetos en la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto de origen</strong> . En el cuadro <strong>Nombre de objeto de origen</strong> , haga clic en el objeto que se va a copiar. Si deja en blanco el argumento <strong>Tipo de objeto de origen</strong> , deje también en blanco este argumento. Si ejecuta una macro que contiene la acción <strong>CopiarObjeto</strong> en una base de datos de biblioteca, Access primero busca el objeto con este nombre en la base de datos de biblioteca y después en la base de datos actual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Debe especificar un valor para uno o los dos argumentos **Base de datos de destino** y **Nombre nuevo** de esta acción.

Si deja en blanco los argumentos **Tipo del objeto de origen** y **Nombre del objeto de origen**, Access copia el objeto seleccionado en el panel de navegación. Para seleccionar un objeto en el panel de navegación, puede usar la acción **SeleccionarObjeto** con el argumento En panel de navegación establecido en **Sí**.

La acción **CopiarObjeto** es similar a realizar los siguientes pasos manualmente:

1. Seleccione un objeto en el Panel de navegación.

2. En la pestaña Home, en el grupo Clipboard, haga clic en Copy.

3. En la misma ficha, haga clic en **Pegar**.El cuadro de diálogo **Pegar como** aparece de modo que pueda proporcionarle un nombre nuevo al objeto. La acción **CopiarObjeto** realiza todos estos pasos automáticamente.

> [!NOTE]
> [!NOTA] Al copiar páginas de acceso a datos, la acción **CopiarObjeto** copia solo el vínculo al archivo .htm asociado, no al archivo en sí.

La ruta y el nombre de archivo de la base de datos de destino deben existir antes de que la macro ejecute la acción **CopiarObjeto**. Si no existen, Access muestra un mensaje de error.

Para ejecutar la acción **CopiarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **CopyObject** del objeto **DoCmd**.

También se puede copiar manualmente un objeto seleccionado en el panel de navegación o un objeto que está abierto actualmente, haciendo clic en el **Botón de Microsoft Office** y en **Guardar como**. Este comando realizará una copia del objeto únicamente en la base de datos activa. En el cuadro de diálogo **Guardar como**, escriba el nombre para la copia y elija el tipo de objeto con el que desea guardarla. Si ya se ha guardado el objeto original y guarda la copia en la base de datos activa con un nombre nuevo, la versión original se conservará con su nombre antiguo.

Para copiar manualmente un objeto a una base de datos de Access diferente:

1. En la ficha **Datos externos**, en el grupo **Exportar**, haga clic en **Más** y, a continuación, en **Base de datos de Access**.

2. En el cuadro de diálogo **Exportar - Base de datos de Access**, escriba el nombre del archivo de la base de datos de destino.-o bien-Haga clic en **Examinar** para mostrar el cuadro de diálogo **Guardar archivo**, ubique la base de datos de destino y haga clic en **Guardar**.

3. En el cuadro de diálogo **Exportar - Base de datos de Access**, haga clic en **Aceptar**. Aparece el cuadro de diálogo **Exportar**.

4. En el cuadro de diálogo **Exportar**, escriba un nombre para el objeto de la base de datos de destino. Elija las opciones aplicables, como **Exportar definición y datos** o **Sólo definición** para las tablas. Cuando haya terminado, haga clic en **Aceptar**.

