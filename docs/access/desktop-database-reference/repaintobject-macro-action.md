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
ms.openlocfilehash: 4371ce5482b775ad9c022eeda8202c4b2e0f800d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485251"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="a6ee5-102">RepintarObjeto (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a6ee5-102">RepaintObject Macro Action</span></span>


<span data-ttu-id="a6ee5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6ee5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6ee5-p101">Puede usar la acción **RepintarObjeto** para completar cualquier actualización de pantalla que quede pendiente para un objeto de base de datos especificado o el objeto de base de datos activo si no hay ninguno especificado. Esas actualizaciones incluyen todos los cálculos pendientes de los controles del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p101">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified. Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="a6ee5-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="a6ee5-106">Setting</span></span>

<span data-ttu-id="a6ee5-107">La acción **RepintarObjeto** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6ee5-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="a6ee5-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a6ee5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6ee5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ee5-110"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="a6ee5-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ee5-p102">Tipo del objeto que se va a repintar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Deje este argumento en blanco para seleccionar el objeto activo.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ee5-114"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="a6ee5-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ee5-p103">Nombre del objeto que se va a repintar. En el cuadro <strong>Nombre del objeto</strong> se muestran todos los objetos de la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p103">The name of the object to repaint. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a6ee5-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6ee5-118">Remarks</span></span>

<span data-ttu-id="a6ee5-p104">Microsoft Access espera a completar las actualizaciones de pantalla pendientes hasta que termina otras tareas pendientes. Con esta acción, se puede forzar a que se vuelvan a pintar inmediatamente los controles del objeto especificado. Podrá usar esta acción en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

  - <span data-ttu-id="a6ee5-p105">Cuando use la acción **EstablecerValor** para cambiar valores en varios controles. Es posible que Access no muestre los cambios de forma inmediata, especialmente si hay otros controles (por ejemplo, controles calculados) que dependan de los valores de los controles modificados.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

  - <span data-ttu-id="a6ee5-p106">Cuando desee estar seguro de que el formulario que está viendo muestra los datos de todos sus controles. Por ejemplo, los controles que contienen objetos OLE no muestran sus datos de forma inmediata después de abrirse un formulario.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="a6ee5-p107">Esta acción no genera una nueva consulta de la base de datos, por lo que no muestra los registros nuevos o cambiados ni quita los registros eliminados de la tabla o consulta subyacente del objeto. Use la acción <STRONG>NuevaConsulta</STRONG> para volver a consultar el origen del objeto o uno de sus controles. Use la acción <STRONG>MostrarTodosRegistros</STRONG> para mostrar los registros más recientes y quitar los filtros que se hayan aplicado.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the <STRONG>Requery</STRONG> action to requery the source of the object or one of its controls. Use the <STRONG>ShowAllRecords</STRONG> action to display the most recent records and remove any applied filters.</span></span></P>
> <LI>
> <P><span data-ttu-id="a6ee5-129">La acción <STRONG>RepintarObjeto</STRONG> no tiene el mismo efecto que hacer clic en <STRONG>Actualizar</STRONG> en el grupo <STRONG>Registros</STRONG> de la ficha <STRONG>Inicio</STRONG>, lo que muestra todos los cambios realizados por los usuarios en los registros que se muestran actualmente en los formularios y hojas de datos.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-129">The <STRONG>RepaintObject</STRONG> action doesn't have the same effect as clicking <STRONG>Refresh</STRONG> in the <STRONG>Records</STRONG> group on the <STRONG>Home</STRONG> tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span></P></LI></UL>



<span data-ttu-id="a6ee5-130">Para ejecutar la acción **RepintarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RepaintObject** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="a6ee5-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>
