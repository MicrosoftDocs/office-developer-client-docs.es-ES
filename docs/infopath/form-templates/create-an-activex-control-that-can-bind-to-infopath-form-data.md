---
title: Crear un control ActiveX que pueda enlazar a datos de formulario de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Se pueden hospedar controles ActiveX en formularios de InfoPath diseñados para abrirse en el editor de InfoPath. Estos controles pueden existir previamente (con algunas restricciones) o escribirse específicamente para InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300192"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="fe9f0-104">Crear un control ActiveX que pueda enlazar a datos de formulario de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fe9f0-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="fe9f0-p102">Se pueden hospedar controles ActiveX en formularios de InfoPath diseñados para abrirse en el editor de InfoPath. Estos controles pueden existir previamente (con algunas restricciones) o escribirse específicamente para InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-p102">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor. These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="fe9f0-107">Escribir un control ActiveX</span><span class="sxs-lookup"><span data-stu-id="fe9f0-107">Write an ActiveX Control</span></span>

<span data-ttu-id="fe9f0-108">Tal como ocurre con otros controles en InfoPath, los controles ActiveX deben ser compatibles con las interfaces existentes del Modelo de objetos componentes (COM):</span><span class="sxs-lookup"><span data-stu-id="fe9f0-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="fe9f0-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-109">**IDispatch**</span></span>
    
- <span data-ttu-id="fe9f0-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="fe9f0-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="fe9f0-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="fe9f0-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="fe9f0-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="fe9f0-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-115">**IViewObject**</span></span>
    
- <span data-ttu-id="fe9f0-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-116">**IOleObject**</span></span>
    
- <span data-ttu-id="fe9f0-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="fe9f0-118">Para que InfoPath actualice las propiedades del Modelo de objetos de documentos (DOM) en el momento en que cambian en el control, el control debe implementar las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe9f0-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="fe9f0-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="fe9f0-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="fe9f0-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="fe9f0-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="fe9f0-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="fe9f0-123">Asimismo, existen dos interfaces COM específicas de InfoPath que permiten una mejor integración de controles:</span><span class="sxs-lookup"><span data-stu-id="fe9f0-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="fe9f0-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="fe9f0-124">IInfoPathControl</span></span>](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [<span data-ttu-id="fe9f0-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="fe9f0-125">IInfoPathControlSite</span></span>](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="fe9f0-126">Agregar un control ActiveX al entorno de diseño de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fe9f0-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="fe9f0-p103">El comando **Agregar o quitar controles personalizados** en el panel de tareas **Controles** permite usar el **Asistente para agregar un control personalizado** para agregar un control personalizado. Al usar el asistente, se puede seleccionar un control ActiveX que ya se haya registrado o buscar otros controles personalizados en el Catálogo de soluciones de Office. Después de seleccionar un control, se pueden especificar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-p103">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control. By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace. After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="fe9f0-130">Especificar un archivo CAB para instalar el control ActiveX con la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="fe9f0-131">Especificar una propiedad de enlace para enlazar al XML.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="fe9f0-132">Especificar una propiedad que se use para habilitar o deshabilitar el control en respuesta a las reglas o firmas digitales, lo cual puede resultar útil, por ejemplo, cuando el XML no está presente o cuando se usa formato condicional.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="fe9f0-133">Especificar el enlace del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fe9f0-134">[!NOTA] Si está desarrollando un control ActiveX y lo agrega al panel de tareas **Controles** de InfoPath, no se podrá volver a generar el control ActiveX hasta que se cierre InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="fe9f0-135">Implementar un Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="fe9f0-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="fe9f0-p104">Para distribuir un control ActiveX, es posible escribir un instalador que instale el control en el equipo de destino y copie el archivo de Plantilla de control (ICT) de InfoPath y el archivo CAB en la carpeta del usuario, \Users\\<nombreUsuario\>\AppData\Local\Microsoft\InfoPath\Controls. Se debe tener en cuenta que si hay dos o más programadores que colaboran en el desarrollo de formularios que usan controles ActiveX, cada programador debe tener los controles que se agregaron al entorno de desarrollo de InfoPath, o no podrán modificar las propiedades de los controles desde InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-p104">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls. Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe9f0-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe9f0-138">See also</span></span>

<span data-ttu-id="fe9f0-139">Práctica 6: Agregar controles ActiveX en InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="fe9f0-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="fe9f0-140">Crear un control personalizado de InfoPath con C# y .NET (Blog del equipo de InfoPath)</span><span class="sxs-lookup"><span data-stu-id="fe9f0-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

