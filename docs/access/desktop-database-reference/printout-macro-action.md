---
title: Imprimir (acción de macro)
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301410"
---
# <a name="printout-macro-action"></a><span data-ttu-id="6af62-102">Imprimir (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="6af62-102">PrintOut macro action</span></span>

<span data-ttu-id="6af62-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6af62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6af62-p101">Puede usar la acción **Imprimir** para imprimir el objeto activo de la base de datos abierta. Puede imprimir hojas de datos, informes, formularios, páginas de acceso a datos y módulos.</span><span class="sxs-lookup"><span data-stu-id="6af62-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="6af62-106">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="6af62-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="6af62-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="6af62-107">Setting</span></span>

<span data-ttu-id="6af62-108">La acción **Imprimir** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6af62-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6af62-109">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="6af62-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6af62-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6af62-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6af62-111"><strong>Intervalo de impresión</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-p102">Intervalo que se va a imprimir. Haga clic en <strong>Todo</strong> (el usuario puede imprimir todo el objeto), <strong>Selección</strong> (el usuario puede imprimir la parte del objeto que se haya seleccionado) o <strong>Páginas</strong> (el usuario puede especificar un intervalo de páginas en los argumentos <strong>Desde la página</strong> y <strong>Hasta la página</strong>) en el cuadro <strong>Intervalo de impresión</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Todo</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-p102">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af62-115"><strong>Desde página</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-p103">Primera página que se va a imprimir. La impresión comienza al principio de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-p103">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af62-119"><strong>Hasta página</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-p104">Última página que se va a imprimir. La impresión se detiene en la parte inferior de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-p104">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af62-123"><strong>Calidad de impresión</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-124">Calidad de la impresión.</span><span class="sxs-lookup"><span data-stu-id="6af62-124">The print quality.</span></span> <span data-ttu-id="6af62-125">Haga clic en <strong>Alta</strong>, <strong>Media</strong>, <strong>Baja</strong> o <strong>Borrador</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-125">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="6af62-126">Cuanto menor sea la calidad, más rápido se imprimirá el objeto.</span><span class="sxs-lookup"><span data-stu-id="6af62-126">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="6af62-127">El valor predeterminado es <strong>Alta</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-127">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af62-128"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-129">Número de copias que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="6af62-129">The number of copies to print.</span></span> <span data-ttu-id="6af62-130">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="6af62-130">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af62-131"><strong>Intercalar copias</strong></span><span class="sxs-lookup"><span data-stu-id="6af62-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="6af62-p107">Haga clic en <strong>Sí</strong> (para intercalar las copias impresas) o en <strong>No</strong> (para no intercalar las copias). El objeto se imprime más rápido si este argumento está establecido en <strong>No</strong>. El valor predeterminado es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af62-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6af62-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6af62-135">Remarks</span></span>

<span data-ttu-id="6af62-p108">Esta acción es similar a seleccionar un objeto, hacer clic en la pestaña **Archivo** y, a continuación, hacer clic en **Imprimir**. Con esta acción, no obstante, no aparece el cuadro de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="6af62-p108">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="6af62-138">[!SUGERENCIA] Si utiliza frecuentemente determinados valores de impresión, cree una macro que contenga una acción **Imprimir** con esos valores en sus argumentos.</span><span class="sxs-lookup"><span data-stu-id="6af62-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="6af62-p109">Los argumentos de esta acción corresponden a las opciones del cuadro de diálogo **Imprimir**. No obstante, a diferencia de la acción **BuscarRegistro** y del cuadro de diálogo **Buscar y reemplazar**, los valores de los argumentos no se comparten con las opciones del cuadro de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="6af62-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="6af62-141">Para ejecutar la acción **Imprimir** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **PrintOut** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="6af62-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

