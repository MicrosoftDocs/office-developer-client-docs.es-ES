---
title: Establecer propiedades de formularios, informes y controles
TOCTitle: Set form, report, and control properties
description: Cada formulario, informe, sección y control tienen valores de propiedad que se pueden cambiar para alterar el aspecto o comportamiento de ese elemento determinado en Access 2013.
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701693"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="62247-103">Establecer propiedades de formularios, informes y controles</span><span class="sxs-lookup"><span data-stu-id="62247-103">Set form, report, and control properties</span></span>

<span data-ttu-id="62247-104">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62247-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62247-p101">Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="62247-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="62247-107">Establecer las propiedades</span><span class="sxs-lookup"><span data-stu-id="62247-107">Set properties</span></span>

1. <span data-ttu-id="62247-p102">En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:</span><span class="sxs-lookup"><span data-stu-id="62247-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="62247-110">Uno o varios controles.</span><span class="sxs-lookup"><span data-stu-id="62247-110">One or more controls.</span></span> <span data-ttu-id="62247-111">Para seleccionar varios controles, mantenga presionada la tecla MAYÚS y seleccione los controles o, arrastre el puntero del mouse sobre los controles que desea seleccionar.</span><span class="sxs-lookup"><span data-stu-id="62247-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="62247-112">Si selecciona varios controles, la hoja de propiedades mostrará sólo aquellas propiedades que los controles seleccionados tienen en común.</span><span class="sxs-lookup"><span data-stu-id="62247-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="62247-113">Una sección.</span><span class="sxs-lookup"><span data-stu-id="62247-113">One section.</span></span> <span data-ttu-id="62247-114">Elija el selector de sección de la sección que desea seleccionar.</span><span class="sxs-lookup"><span data-stu-id="62247-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="62247-115">El formulario o informe completo.</span><span class="sxs-lookup"><span data-stu-id="62247-115">The entire form or report.</span></span> <span data-ttu-id="62247-116">Elija el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="62247-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="62247-117">Mostrar la hoja de propiedades por bien el objeto o sección y, a continuación, elija **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="62247-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="62247-118">Elija la propiedad para la que desea establecer el valor y, a continuación, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="62247-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="62247-119">En el cuadro de la propiedad, escriba el valor o expresión apropiado.</span><span class="sxs-lookup"><span data-stu-id="62247-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="62247-120">Si el cuadro de la propiedad contiene una flecha, elija la flecha y, a continuación, elija un valor en la lista.</span><span class="sxs-lookup"><span data-stu-id="62247-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="62247-121">Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, elija para mostrar un generador o para mostrar un cuadro de diálogo que le una opción de elegir generadores.</span><span class="sxs-lookup"><span data-stu-id="62247-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="62247-122">Por ejemplo, puede usar el Generador de código, Generador de macros, o el Generador de consultas para establecer algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="62247-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="62247-123">Sugerencias </span><span class="sxs-lookup"><span data-stu-id="62247-123">Tips</span></span>

- <span data-ttu-id="62247-124">Microsoft Access dispone de un cuadro **Zoom** para escribir y presentar expresiones u otros valores de propiedades largas.</span><span class="sxs-lookup"><span data-stu-id="62247-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="62247-125">Para mostrar el cuadro **Zoom** , elija un cuadro de propiedad en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="62247-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="62247-126">Presione MAYÚS + F2 o con el botón secundario y, a continuación, elija **Zoom** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62247-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="62247-127">Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.</span><span class="sxs-lookup"><span data-stu-id="62247-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="62247-128">Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="62247-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="62247-129">Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control.</span><span class="sxs-lookup"><span data-stu-id="62247-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="62247-130">Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="62247-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

