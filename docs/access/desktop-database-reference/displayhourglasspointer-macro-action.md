---
title: MostrarCursorDeRelojDeArena (acción de macro)
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 159e9f1b4cf7beab96a463ff476b4edf577e1371
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926937"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="e6611-102">MostrarCursorDeRelojDeArena (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e6611-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="e6611-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6611-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6611-p101">Puede usar la acción **MostrarCursorDeRelojDeArena** para cambiar el puntero del mouse por la imagen de un reloj de arena (u otro icono que se elija) mientras se ejecuta una macro. Esta acción puede proporcionar una indicación visual de que la macro está ejecutándose. Resulta especialmente útil cuando una acción de macro o la propia macro tarda mucho tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e6611-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="e6611-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="e6611-107">Setting</span></span>

<span data-ttu-id="e6611-108">La acción **MostrarCursorDeRelojDeArena** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="e6611-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6611-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="e6611-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e6611-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6611-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6611-111"><strong>Reloj de arena activo</strong></span><span class="sxs-lookup"><span data-stu-id="e6611-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="e6611-p102">Haga clic en <strong>Sí</strong> (para mostrar el icono) o en <strong>No</strong> (para mostrar el puntero normal del mouse) en el cuadro <strong>Reloj de arena activo</strong> de la sección <strong>Argumentos de acción</strong> en el panel Generador de macros. El valor predeterminado es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6611-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6611-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6611-114">Remarks</span></span>

<span data-ttu-id="e6611-115">Esta acción se suele usar si se ha desactivado el eco mediante la acción **Eco**.</span><span class="sxs-lookup"><span data-stu-id="e6611-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="e6611-116">Cuando el eco está desactivado, Access suspende las actualizaciones de pantalla hasta que finalice la macro.</span><span class="sxs-lookup"><span data-stu-id="e6611-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="e6611-117">Access restablece automáticamente el argumento **Reloj de arena activo** en **No** cuando la macro deja de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e6611-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="e6611-p104">En Microsoft Windows, es el icono que se establece para **Ocupado** en el cuadro de diálogo **Propiedades de Mouse** del Panel de control de Windows. El icono predeterminado para todos los sistemas operativos Windows es un reloj de arena animado.</span><span class="sxs-lookup"><span data-stu-id="e6611-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="e6611-120">Si lo desea, puede elegir otro icono.</span><span class="sxs-lookup"><span data-stu-id="e6611-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="e6611-121">Para ejecutar la acción **MostrarCursorDeRelojDeArena** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RelojDeArena** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e6611-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

