---
title: Establecer propiedades de formularios, informes y controles
TOCTitle: Set form, report, and control properties
description: Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado en Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308739"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="92225-103">Establecer propiedades de formularios, informes y controles</span><span class="sxs-lookup"><span data-stu-id="92225-103">Set form, report, and control properties</span></span>

<span data-ttu-id="92225-104">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92225-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92225-p101">Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="92225-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="92225-107">Establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="92225-107">Set properties</span></span>

1. <span data-ttu-id="92225-p102">En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:</span><span class="sxs-lookup"><span data-stu-id="92225-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="92225-110">Uno o más controles.</span><span class="sxs-lookup"><span data-stu-id="92225-110">One or more controls.</span></span> <span data-ttu-id="92225-111">Para seleccionar controles múltiples, se puede hacer clic en los controles con la tecla MAYÚS presionada o arrastrar el puntero del ratón sobre los controles que desea seleccionar.</span><span class="sxs-lookup"><span data-stu-id="92225-111">To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="92225-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span><span class="sxs-lookup"><span data-stu-id="92225-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="92225-113">Una sección.</span><span class="sxs-lookup"><span data-stu-id="92225-113">One section.</span></span> <span data-ttu-id="92225-114">Haga clic en el selector de sección de la sección que quiere seleccionar.</span><span class="sxs-lookup"><span data-stu-id="92225-114">Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="92225-115">Todo el formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="92225-115">The entire form or report.</span></span> <span data-ttu-id="92225-116">Haga clic en el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="92225-116">Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="92225-117">Muestre la hoja de propiedades haciendo clic con el botón secundario en el objeto o sección y luego eligiendo **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="92225-117">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="92225-118">Elija la propiedad para la que desea establecer el valor, y luego haga una de las siguientes cosas:</span><span class="sxs-lookup"><span data-stu-id="92225-118">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="92225-119">En el cuadro de propiedades, escriba el valor o expresión apropiados.</span><span class="sxs-lookup"><span data-stu-id="92225-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="92225-120">Si el cuadro de la propiedad contiene una flecha, haga clic en la flecha y luego elija un valor de la lista.</span><span class="sxs-lookup"><span data-stu-id="92225-120">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="92225-121">Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, haga clic en el mismo para mostrar un generador o para mostrar un cuadro de diálogo que le dé la opción de elegir generadores.</span><span class="sxs-lookup"><span data-stu-id="92225-121">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="92225-122">Por ejemplo, puede usar el Generador de código, Generador de macros o Generador de consultas para establecer algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="92225-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="92225-123">Sugerencias</span><span class="sxs-lookup"><span data-stu-id="92225-123">Tips</span></span>

- <span data-ttu-id="92225-124">Microsoft Access proporciona un cuadro de **Zoom** para escribir y ver expresiones u otros valores de propiedades largos.</span><span class="sxs-lookup"><span data-stu-id="92225-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="92225-125">Para mostrar el cuadro **Zoom**, haga clic en un cuadro de propiedad en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="92225-125">To display the **Zoom** box, click a property box in the property sheet.</span></span> <span data-ttu-id="92225-126">Presione MAYÚS+F2, o haga clic con el botón secundario y luego elija **Zoom** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="92225-126">Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="92225-127">Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.</span><span class="sxs-lookup"><span data-stu-id="92225-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="92225-128">Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="92225-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="92225-129">Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control.</span><span class="sxs-lookup"><span data-stu-id="92225-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="92225-130">Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="92225-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

