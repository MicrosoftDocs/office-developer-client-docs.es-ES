---
title: RepintarObjeto (acción de macro)
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2ef6c5f38064ae3253cd7e0e58732f63294ceb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306688"
---
# <a name="repaintobject-macro-action"></a>RepintarObjeto (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **RepintarObjeto** para completar cualquier actualización de pantalla que quede pendiente para un objeto de base de datos especificado o el objeto de base de datos activo si no hay ninguno especificado. Esas actualizaciones incluyen todos los cálculos pendientes de los controles del objeto.

## <a name="setting"></a>Setting

La acción **RepintarObjeto** tiene los siguientes argumentos.

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
<td><p>Tipo del objeto que se va a repintar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Deje este argumento en blanco para seleccionar el objeto activo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>Nombre del objeto que se va a repintar. En el cuadro <strong>Nombre del objeto</strong> se muestran todos los objetos de la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Microsoft Access espera a completar las actualizaciones de pantalla pendientes hasta que termina otras tareas pendientes. Con esta acción, se puede forzar a que se vuelvan a pintar inmediatamente los controles del objeto especificado. Podrá usar esta acción en los siguientes casos:

- Cuando use la acción **EstablecerValor** para cambiar valores en varios controles. Es posible que Access no muestre los cambios de forma inmediata, especialmente si hay otros controles (por ejemplo, controles calculados) que dependan de los valores de los controles modificados.

- Cuando desee estar seguro de que el formulario que está viendo muestra los datos de todos sus controles. Por ejemplo, los controles que contienen objetos OLE no muestran sus datos de forma inmediata después de abrirse un formulario.

> [!NOTE]
> - Esta acción no genera una nueva consulta de la base de datos, por lo que no muestra los registros nuevos o cambiados ni quita los registros eliminados de la tabla o consulta subyacente del objeto. Use la acción **NuevaConsulta** para volver a consultar el origen del objeto o uno de sus controles. Use la acción **MostrarTodosRegistros** para mostrar los registros más recientes y quitar los filtros que se hayan aplicado.
> - La acción **RepintarObjeto** no tiene el mismo efecto que hacer clic en **Actualizar** en el grupo **Registros** de la ficha **Inicio**, lo que muestra todos los cambios realizados por los usuarios en los registros que se muestran actualmente en los formularios y hojas de datos.

Para ejecutar la acción **RepintarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RepaintObject** del objeto **DoCmd**.

