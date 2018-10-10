---
title: Conjunto de formulario, informe y propiedades de control
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484508"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="7007d-102">Conjunto de formulario, informe y propiedades de control</span><span class="sxs-lookup"><span data-stu-id="7007d-102">Set form, report, and control properties</span></span>

<span data-ttu-id="7007d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7007d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7007d-p101">Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7007d-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="7007d-106">Establecer las propiedades</span><span class="sxs-lookup"><span data-stu-id="7007d-106">Set properties</span></span>

1. <span data-ttu-id="7007d-p102">En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:</span><span class="sxs-lookup"><span data-stu-id="7007d-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="7007d-p103">Uno o más controles. Para seleccionar controles múltiples, se puede hacer clic en los controles con la tecla MAYÚS presionada o arrastrar el puntero del mouse sobre los controles que desea seleccionar. Si selecciona múltiples controles, la hoja de propiedades mostrará sólo aquellas propiedades que tienen en común los controles seleccionados.</span><span class="sxs-lookup"><span data-stu-id="7007d-p103">One or more controls. To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select. If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="7007d-p104">Una sección. Haga clic en el selector de sección de la sección que desea seleccionar.</span><span class="sxs-lookup"><span data-stu-id="7007d-p104">One section. Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="7007d-p105">El formulario o informe completo. Haga clic en el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="7007d-p105">The entire form or report. Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="7007d-116">Muestre la hoja de propiedades haciendo clic con el botón secundario en el objeto o sección y luego eligiendo **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7007d-116">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="7007d-117">Elija la propiedad para la que desea establecer el valor, y luego haga una de las siguientes cosas:</span><span class="sxs-lookup"><span data-stu-id="7007d-117">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="7007d-118">En el cuadro de la propiedad, escriba el valor o expresión apropiado.</span><span class="sxs-lookup"><span data-stu-id="7007d-118">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="7007d-119">Si el cuadro de la propiedad contiene una flecha, haga clic en la flecha y luego elija un valor de la lista.</span><span class="sxs-lookup"><span data-stu-id="7007d-119">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="7007d-p106">Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, haga clic en el mismo para mostrar un generador o para mostrar un cuadro de diálogo que le dé la opción de elegir generadores. Por ejemplo, puede usar el Generador de código, Generador de macros, o el Generador de consultas para establecer algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7007d-p106">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders. For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="7007d-122">Sugerencias </span><span class="sxs-lookup"><span data-stu-id="7007d-122">Tips</span></span>

- <span data-ttu-id="7007d-p107">Microsoft Access dispone de un cuadro **Zoom** para escribir y presentar expresiones u otros valores de propiedades largas. Para mostrar el cuadro **Zoom**, haga clic en un cuadro de propiedad en la hoja de propiedades. Luego presione MAYÚS+F2, o haga clic con el botón secundario y luego elija **Zoom** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="7007d-p107">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings. To display the **Zoom** box, click a property box in the property sheet. Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="7007d-126">Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.</span><span class="sxs-lookup"><span data-stu-id="7007d-126">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="7007d-127">Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="7007d-127">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="7007d-p108">Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control. Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta. Para obtener más información sobre cómo se heredan las propiedades, vea Cómo se relacionan las propiedades de control con las propiedades de sus campos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="7007d-p108">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound. If the settings are different, the form or report settings typically override those in the table or query. For more information about how properties are inherited, see How control properties relate to properties in their underlying fields.</span></span>

