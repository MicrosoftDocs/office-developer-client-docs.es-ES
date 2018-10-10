---
title: Cuadro de diálogo de propiedades personalizadas del Control ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485335"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="e080b-102">Cuadro de diálogo de propiedades personalizadas del Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="e080b-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="e080b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e080b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e080b-p101">Al establecer las propiedades de un control ActiveX, puede necesitar o preferir el uso del cuadro de diálogo de propiedades personalizadas del control. Este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades de la hoja de propiedades de Microsoft Access para establecer las propiedades del control ActiveX en la vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="e080b-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="e080b-106">[!NOTA] Esta información sólo tiene aplicación para controles ActiveX en el entorno de una base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e080b-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="e080b-107">Dos modos de establecer las propiedades</span><span class="sxs-lookup"><span data-stu-id="e080b-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="e080b-p102">La razón de ser del cuadro de diálogo de propiedades personalizadas es que no todas las aplicaciones que usan controles ActiveX ofrecen una hoja de propiedades como la de Microsoft Access. El cuadro de diálogo de propiedades personalizadas ofrece una interfaz para establecer las propiedades clave del control sea cual sea la interfaz suministrada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e080b-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="e080b-110">Para algunas propiedades de los controles ActiveX, es posible elegir establecer las propiedades en:</span><span class="sxs-lookup"><span data-stu-id="e080b-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="e080b-111">La hoja de propiedades de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e080b-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="e080b-112">El cuadro de diálogo de propiedades personalizadas del control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e080b-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="e080b-p103">En algunos casos, el cuadro de diálogo de propiedades personalizadas es el único medio disponible para establecer una propiedad en la vista Diseño. Ésta es normalmente la situación cuando la interfaz necesaria para establecer una propiedad no funciona dentro de la hoja de propiedades de Microsoft Access. Por ejemplo, la propiedad **FuenteDeCuadrícula (GridFont)** del control Calendar tiene varios argumentos; no es posible establecer más de un argumento para cada propiedad en la hoja de propiedades de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e080b-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="e080b-116">Localizar el Cuadro de diálogo de propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="e080b-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="e080b-p104">No todos los controles ActiveX ofrecen un cuadro de diálogo de propiedades personalizadas. Para ver si un control ofrece este cuadro de diálogo de propiedades personalizadas, busque la propiedad **Personalizado (Custom)** en la hoja de propiedades de Microsoft Access para este control. Si la lista de propiedades incluye **Personalizado**, entonces el control dispone de cuadro de diálogo de propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e080b-p104">Not all ActiveX controls provide a custom properties dialog box. To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control. If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="e080b-120">Utilización del Cuadro de diálogo de propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="e080b-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="e080b-p105">Después de hacer clic en el cuadro de la propiedad **Personalizado** en la hoja de propiedades de Microsoft Access, haga clic en el botón **Generar** situado a la derecha del cuadro de la propiedad para mostrar el cuadro de diálogo de propiedades personalizadas del control, a menudo presentada en forma de cuadro de diálogo con fichas. Seleccione la ficha que contenga la interfaz para las propiedades que desee establecer.</span><span class="sxs-lookup"><span data-stu-id="e080b-p105">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box. Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="e080b-p106">Después de realizar cambios en una ficha, normalmente se pueden aplicar dichos cambios inmediatamente haciendo clic en el botón **Aplicar** (si está presente). Puede hacer clic en otras pestañas para establecer otras propiedades según sus necesidades. Para confirmar todos los cambios en el cuadro de diálogo de propiedades personalizadas, haga clic en el botón **Aceptar**. Para volver a la hoja de propiedades de Microsoft Access sin cambiar los valores de ninguna propiedad, haga clic en el botón **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="e080b-p106">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided). You can click other tabs to set other properties as needed. To approve all changes made in the custom properties dialog box, click the **OK** button. To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="e080b-p107">También puede ver el cuadro de diálogo de propiedades personalizadas haciendo clic en el subcomando **Propiedades** del comando **Objeto** del control ActiveX (por ejemplo, **Objeto Control de calendario**) del menú **Edición**, o haciendo clic en este mismo subcomando en el menú contextual del control ActiveX. Además, algunas propiedades de la hoja de propiedades de Microsoft Access para el control ActiveX, como la propiedad **GridFontColor** del control Calendar, disponen de un botón **Generar** situado a la derecha del cuadro de la propiedad. Al hacer clic en el botón **Generar**, se muestra el cuadro de diálogo de propiedades personalizadas, con la ficha correspondiente ya seleccionada (por ejemplo, **Colores**).</span><span class="sxs-lookup"><span data-stu-id="e080b-p107">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

