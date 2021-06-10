---
title: EstablecerAdvertencias (acción de macro)
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308662"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="bac57-102">EstablecerAdvertencias (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="bac57-102">SetWarnings macro action</span></span>

<span data-ttu-id="bac57-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bac57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bac57-104">Puede usar la acción **EstablecerAdvertencias** para activar y desactivar los mensajes del sistema.</span><span class="sxs-lookup"><span data-stu-id="bac57-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="bac57-105">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="bac57-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="bac57-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="bac57-106">Setting</span></span>

<span data-ttu-id="bac57-107">La acción **EstablecerAdvertencias** utiliza el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="bac57-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bac57-108">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="bac57-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bac57-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bac57-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bac57-110"><strong>Activar advertencias</strong></span><span class="sxs-lookup"><span data-stu-id="bac57-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="bac57-p101">Especifica si se deben mostrar los mensajes del sistema. Haga clic en <strong>Sí</strong> (para activar los mensajes del sistema) o en <strong>No</strong> (para desactivar los mensajes del sistema) en el cuadro <strong>Activar advertencias</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="bac57-p101">Specifies whether system messages are displayed. Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bac57-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bac57-114">Remarks</span></span>

<span data-ttu-id="bac57-p102">Puede usar esta acción para evitar que los cuadros de mensajes y advertencias modales detengan la macro. No obstante, los mensajes de error siempre se muestran. Además, Microsoft Access muestra también los cuadros de diálogo que requieren alguna entrada que no sea simplemente elegir un botón (como **Aceptar**, **Cancelar**, **Sí** o **No**); por ejemplo, cualquier cuadro de diálogo que requiera que se escriba texto o se seleccione una de varias opciones.</span><span class="sxs-lookup"><span data-stu-id="bac57-p102">You can use this action to prevent modal warnings and message boxes from stopping the macro. However, error messages are always displayed. Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="bac57-p103">Ejecutar esta acción con el argumento **Activar advertencias** establecido en **No** equivale a presionar ENTRAR cuando aparece un cuadro de mensaje o advertencia. Normalmente, se elige un botón **Aceptar** o **Sí** en respuesta al mensaje o advertencia.</span><span class="sxs-lookup"><span data-stu-id="bac57-p103">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed. Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="bac57-120">Cuando termina la macro, Access vuelve a activar automáticamente la presentación de mensajes del sistema.</span><span class="sxs-lookup"><span data-stu-id="bac57-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="bac57-p104">Esta acción se suele utilizar con la acción **Eco**, la cual permite ocultar los resultados de una macro mientras ésta se ejecuta. Puede usar entonces la acción **EstablecerAdvertencias** para ocultar también los cuadros de mensajes y advertencias.</span><span class="sxs-lookup"><span data-stu-id="bac57-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="bac57-p105">[!PRECAUCIóN] Aunque la acción **EstablecerAdvertencias** puede simplificar las interacciones con las macros, se debe tener cuidado con la desactivación de los mensajes del sistema. En algunas situaciones, no deseará continuar con una macro si aparece un determinado mensaje. A menos que esté muy seguro del resultado de todas las acciones de la macro, debería evitar utilizar esta acción.</span><span class="sxs-lookup"><span data-stu-id="bac57-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="bac57-126">Para ejecutar la acción **EstablecerAdvertencias** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SetWarnings** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="bac57-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

