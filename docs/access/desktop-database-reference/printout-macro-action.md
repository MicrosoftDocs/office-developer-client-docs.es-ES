---
title: Imprimir (acción de macro)
TOCTitle: PrintOut Macro Action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6a0aa0ae6d992410d5bed6126bfe49d7e84e9135
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878734"
---
# <a name="printout-macro-action"></a><span data-ttu-id="100f5-102">Imprimir (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="100f5-102">PrintOut Macro Action</span></span>


<span data-ttu-id="100f5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="100f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="100f5-p101">Puede usar la acción **Imprimir** para imprimir el objeto activo de la base de datos abierta. Puede imprimir hojas de datos, informes, formularios, páginas de acceso a datos y módulos.</span><span class="sxs-lookup"><span data-stu-id="100f5-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>


> [!NOTE]
> <P><span data-ttu-id="100f5-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="100f5-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="100f5-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="100f5-108">Setting</span></span>

<span data-ttu-id="100f5-109">La acción **Imprimir** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="100f5-109">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="100f5-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="100f5-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="100f5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="100f5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="100f5-112"><strong>Intervalo de impresión</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-112"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p103">Intervalo que se va a imprimir. Haga clic en <strong>Todo</strong> (el usuario puede imprimir todo el objeto), <strong>Selección</strong> (el usuario puede imprimir la parte del objeto que se haya seleccionado) o <strong>Páginas</strong> (el usuario puede especificar un intervalo de páginas en los argumentos <strong>Desde la página</strong> y <strong>Hasta la página</strong>) en el cuadro <strong>Intervalo de impresión</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Todo</strong>.</span><span class="sxs-lookup"><span data-stu-id="100f5-p103">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="100f5-116"><strong>Desde página</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-116"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p104">Primera página que se va a imprimir. La impresión comienza al principio de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</span><span class="sxs-lookup"><span data-stu-id="100f5-p104">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="100f5-120"><strong>Hasta página</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-120"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p105">Última página que se va a imprimir. La impresión se detiene en la parte inferior de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</span><span class="sxs-lookup"><span data-stu-id="100f5-p105">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="100f5-124"><strong>Calidad de impresión</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-124"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p106">Calidad de la impresión. Haga clic en <strong>Alta</strong>, <strong>Media</strong>, <strong>Baja</strong> o <strong>Borrador</strong>. Cuanto menor sea la calidad, más rápido se imprimirá el objeto. El valor predeterminado es <strong>Alta</strong>.</span><span class="sxs-lookup"><span data-stu-id="100f5-p106">The print quality. Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>. The lower the quality, the faster the object prints. The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="100f5-129"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-129"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p107">Número de copias que se va a imprimir. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="100f5-p107">The number of copies to print. The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="100f5-132"><strong>Intercalar copias</strong></span><span class="sxs-lookup"><span data-stu-id="100f5-132"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="100f5-p108">Haga clic en <strong>Sí</strong> (para intercalar las copias impresas) o en <strong>No</strong> (para no intercalar las copias). El objeto se imprime más rápido si este argumento está establecido en <strong>No</strong>. El valor predeterminado es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="100f5-p108">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="100f5-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="100f5-136">Remarks</span></span>

<span data-ttu-id="100f5-p109">Esta acción es similar a seleccionar un objeto, hacer clic en la pestaña **Archivo** y, a continuación, hacer clic en **Imprimir**. Con esta acción, no obstante, no aparece el cuadro de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="100f5-p109">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>


> [!TIP]
> <P><span data-ttu-id="100f5-139">[!SUGERENCIA] Si utiliza frecuentemente determinados valores de impresión, cree una macro que contenga una acción <STRONG>Imprimir</STRONG> con esos valores en sus argumentos.</span><span class="sxs-lookup"><span data-stu-id="100f5-139">If you have particular print settings you use frequently, create a macro containing a <STRONG>PrintOut</STRONG> action with these settings in its arguments.</span></span></P>



<span data-ttu-id="100f5-p110">Los argumentos de esta acción corresponden a las opciones del cuadro de diálogo **Imprimir**. No obstante, a diferencia de la acción **BuscarRegistro** y del cuadro de diálogo **Buscar y reemplazar**, los valores de los argumentos no se comparten con las opciones del cuadro de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="100f5-p110">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="100f5-142">Para ejecutar la acción **Imprimir** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **PrintOut** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="100f5-142">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

