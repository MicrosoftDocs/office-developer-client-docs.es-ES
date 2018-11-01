---
title: RepintarObjeto (acción de macro)
TOCTitle: RepaintObject Macro Action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 431baa0e98d0ae3a636cb93fd799c3bdf4450816
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882612"
---
# <a name="repaintobject-macro-action"></a>RepintarObjeto (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **RepintarObjeto** para completar cualquier actualización de pantalla que quede pendiente para un objeto de base de datos especificado o el objeto de base de datos activo si no hay ninguno especificado. Esas actualizaciones incluyen todos los cálculos pendientes de los controles del objeto.

## <a name="setting"></a>Configuración

La acción **RepintarObjeto** tiene los siguientes argumentos.

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
> <UL>
> <LI>
> <P>Esta acción no genera una nueva consulta de la base de datos, por lo que no muestra los registros nuevos o cambiados ni quita los registros eliminados de la tabla o consulta subyacente del objeto. Use la acción <STRONG>NuevaConsulta</STRONG> para volver a consultar el origen del objeto o uno de sus controles. Use la acción <STRONG>MostrarTodosRegistros</STRONG> para mostrar los registros más recientes y quitar los filtros que se hayan aplicado.</P>
> <LI>
> <P>La acción <STRONG>RepintarObjeto</STRONG> no tiene el mismo efecto que hacer clic en <STRONG>Actualizar</STRONG> en el grupo <STRONG>Registros</STRONG> de la ficha <STRONG>Inicio</STRONG>, lo que muestra todos los cambios realizados por los usuarios en los registros que se muestran actualmente en los formularios y hojas de datos.</P></LI></UL>



Para ejecutar la acción **RepintarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RepaintObject** del objeto **DoCmd**.

