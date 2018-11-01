---
title: SalirDeAccess (acción de macro)
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d26f8d32e0df350c52ea22dfec44ac7a24c9ecc9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870754"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="e6f89-102">SalirDeAccess (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e6f89-102">QuitAccess Macro Action</span></span>


<span data-ttu-id="e6f89-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6f89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6f89-p101">Puede usar la acción **SalirDeAccess** para salir de Microsoft Access. La acción **SalirDeAccess** también puede especificar una de las varias opciones para guardar objetos de base de datos antes de salir de Access.</span><span class="sxs-lookup"><span data-stu-id="e6f89-p101">You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e6f89-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="e6f89-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="e6f89-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="e6f89-108">Setting</span></span>

<span data-ttu-id="e6f89-109">La acción **SalirDeAccess** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="e6f89-109">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6f89-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="e6f89-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e6f89-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6f89-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6f89-112"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="e6f89-112"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="e6f89-p103">Especifica lo que ocurre con los objetos no guardados cuando se sale de Access. Haga clic en <strong>Preguntar</strong> (para que se muestren cuadros de diálogo en los que se pregunta si se desea guardar cada objeto), <strong>Guardar todo</strong> (para guardar todos los objetos sin que se muestren los cuadros de diálogo) o <strong>Salir</strong> (para abandonar sin guardar ningún objeto) en el cuadro <strong>Opciones</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Guardar todo</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6f89-p103">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6f89-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6f89-116">Remarks</span></span>

<span data-ttu-id="e6f89-117">Access no ejecuta ninguna acción que siga a la acción **SalirDeAccess** de una macro.</span><span class="sxs-lookup"><span data-stu-id="e6f89-117">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="e6f89-p104">Puede usar esta acción para salir de Access sin que se muestren los cuadros de diálogo **Guardar** mediante un comando de menú personalizado o un botón de un formulario. Por ejemplo, supongamos que tiene un formulario principal para mostrar los objetos en un área de trabajo personalizada. Este formulario podría tener un botón **Salir** que ejecutase una macro que contenga la acción **Salir** con el argumento **Opciones** establecido en **Guardar todo**.</span><span class="sxs-lookup"><span data-stu-id="e6f89-p104">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="e6f89-p105">Esta acción tiene el mismo efecto que hacer clic en la pestaña **Archivo** y, a continuación, hacer clic en **Salir**. Si, al hacer clic en este comando, hay algún objeto que no se haya guardado, los cuadros de diálogo que aparecen son los mismos que los que se presentan cuando se usa **Preguntar** para el argumento **Opciones** de la acción **SalirDeAccess**.</span><span class="sxs-lookup"><span data-stu-id="e6f89-p105">This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="e6f89-123">Puede usar la acción **GuardarObjeto** en una macro para guardar un objeto determinado sin tener que salir de Access o cerrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="e6f89-123">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="e6f89-124">Para ejecutar la acción **SalirDeAccess** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Quit** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e6f89-124">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

