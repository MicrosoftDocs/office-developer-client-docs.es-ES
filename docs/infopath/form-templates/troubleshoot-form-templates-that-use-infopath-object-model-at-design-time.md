---
title: Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de diseño
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se diseñan y depuran plantillas de formulario de código administrado que usan el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815970"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a><span data-ttu-id="82044-104">Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de diseño</span><span class="sxs-lookup"><span data-stu-id="82044-104">Troubleshoot form templates that use the InfoPath object model at design time</span></span>

<span data-ttu-id="82044-105">En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se diseñan y depuran plantillas de formulario de código administrado que usan el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust**.</span><span class="sxs-lookup"><span data-stu-id="82044-105">The following sections describe common troubleshooting scenarios you may encounter while designing and debugging managed code form templates that use the InfoPath 2003-compatible object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace.</span></span> 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a><span data-ttu-id="82044-106">No se pueden depurar plantillas de formulario que utilizan llamadas a métodos y propiedades de nivel de seguridad 3 del modelo de objetos ni obtener una vista previa de las mismas</span><span class="sxs-lookup"><span data-stu-id="82044-106">Cannot Preview or Debug Form Templates That Use Calls to Object Model Security Level 3 Methods and Properties</span></span>

<span data-ttu-id="82044-107">Si intenta depurar u obtener una vista previa de un proyecto de código administrado cuyo código invoque miembros del modelo de objetos que requieren plena confianza, InfoPath mostrará el mensaje de error "Excepción de seguridad no controlada en el código del formulario" y el formulario no se abrirá.</span><span class="sxs-lookup"><span data-stu-id="82044-107">If you attempt to debug or preview a managed-code project that contains code that invokes object model members that require full trust, InfoPath will display the error message "An unhandled security exception has occurred in the form's code" and the form will not open.</span></span> <span data-ttu-id="82044-108">Para permitir que la lógica empresarial de la plantilla de formulario se pueda depurar u obtener una vista previa de la misma, deberá establecer el nivel de seguridad en **Plena confianza** y firmar digitalmente la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="82044-108">To allow business logic in the form template to be debugged or previewed, you must set the security level to **Full Trust** and digitally sign the form template.</span></span> <span data-ttu-id="82044-109">Para obtener información detallada acerca de cómo hacer esto, vea [obtener una vista previa y depurar plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="82044-109">For details on how to do this, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span>
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a><span data-ttu-id="82044-110">No se pueden actualizar las expresiones XPath de los controladores de eventos si el valor del parámetro MatchPath se ha eliminado manualmente</span><span class="sxs-lookup"><span data-stu-id="82044-110">Cannot Update XPath Expressions in Event Handlers If the MatchPath Parameter Value Was Deleted Manually</span></span>

<span data-ttu-id="82044-111">Si agrega un controlador de eventos a un campo o grupo y, después, modifica el esquema del origen de datos en el panel de tareas **Campos** de InfoPath de una forma que afecte a ese campo o grupo (por ejemplo, cambiando su nombre o moviéndolo), aparecerá un mensaje que le preguntará si desea actualizar las expresiones XPath del código del formulario.</span><span class="sxs-lookup"><span data-stu-id="82044-111">If you add an event handler to a field or group and later change the schema of the data source in the InfoPath **Fields** task pane in a way that affects that field or group (for example, by renaming or moving it), a message will be displayed asking if you want to update the XPath expressions in your form's code.</span></span> <span data-ttu-id="82044-112">Las expresiones XPath a las que se refiere este mensaje son los valores especificados en el parámetro [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) del atributo [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) , que se utilizan para asociar el controlador de eventos a un campo o grupo del origen de datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="82044-112">The XPath expressions referred to in this message are the values specified in the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) parameter of the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) attribute, which are used to associate the event handler with a field or group in your form's data source.</span></span> <span data-ttu-id="82044-113">No se actualizará ninguna otra expresión XPath del código.</span><span class="sxs-lookup"><span data-stu-id="82044-113">No other XPath expressions in your code will be updated.</span></span> <span data-ttu-id="82044-114">El algoritmo para actualizar las expresiones XPath depende del valor que esté presente en el parámetro **MatchPath** de los atributos **InfoPathEventHandler** que se aplican al código del formulario.</span><span class="sxs-lookup"><span data-stu-id="82044-114">The algorithm for updating the XPath expressions depends on a value being present in the **MatchPath** parameter of the **InfoPathEventHandler** attributes that are applied in your form code.</span></span> <span data-ttu-id="82044-115">Si eliminó manualmente estos valores antes de responder a la pregunta sobre la actualización de las expresiones XPath, InfoPath no podrá actualizar las expresiones XPath automáticamente.</span><span class="sxs-lookup"><span data-stu-id="82044-115">If you manually deleted these values before responding to the prompt to update XPath expressions, InfoPath will not be able to update the XPath expressions automatically.</span></span> <span data-ttu-id="82044-116">Para obtener más información, vea [Agregar un controlador de eventos con el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="82044-116">For more information, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a><span data-ttu-id="82044-117">No se puede llamar a miembros del modelo de objetos compatible con InfoPath 2003 en un subproceso separado</span><span class="sxs-lookup"><span data-stu-id="82044-117">Cannot Call Members of the InfoPath 2003 Compatible Object Model on a Separate Thread</span></span>

<span data-ttu-id="82044-p103">El modelo de objetos de InfoPath no admite las llamadas en un subproceso separado. Por ejemplo, el ejemplo de código siguiente, que llama a una función denominada LaunchOMFunction que a su vez llama a miembros del modelo de objetos de InfoPath, no se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="82044-p103">The InfoPath 2003-compatible object model does not support calls on a separate thread. For example, the following code, which calls a function named LaunchOMFunction that calls members of the InfoPath object model, will not run.</span></span> 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

<span data-ttu-id="82044-p104">No obstante, si es necesario, existe una forma de superar esta limitación. Para obtener más información, vea [Compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="82044-p104">When necessary, there is a way to work around this limitation. For information, see [Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a><span data-ttu-id="82044-122">La omisión de parámetros opcionales da lugar a un error de generación en Visual Basic y Visual C#</span><span class="sxs-lookup"><span data-stu-id="82044-122">Omitting Optional Parameters Causes a Build Error in Visual Basic and Visual C#</span></span>

<span data-ttu-id="82044-p105">Si un miembro del modelo de objetos de InfoPath contiene un parámetro opcional y no especifica un valor para ese parámetro, deberá pasar el campo **Type.Missing** de ese parámetro. Si no se pasa el campo **Type.Missing** al omitir un valor real, se producirá un error de generación. Esto es aplicable tanto al código escrito en Visual Basic como en Visual C#. Para obtener más información y ejemplos, vea la sección "Transmitir parámetros opcionales a miembros del modelo de objetos de InfoPath" del tema [Modelos de objetos compatibles con InfoPath 2003](infopath-2003-compatible-object-models.md).</span><span class="sxs-lookup"><span data-stu-id="82044-p105">If an InfoPath object model member contains an optional parameter, and you do not specify a value for that parameter, you must pass the **Type.Missing** field for that parameter instead. Failure to pass the **Type.Missing** field when an actual value is omitted will result in a build error. This is true for code written in both Visual Basic and Visual C#. For more information and examples see the "Passing Optional Parameters to InfoPath Object Model Members" section in the [InfoPath 2003 Compatible Object Models](infopath-2003-compatible-object-models.md) topic.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82044-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="82044-127">See also</span></span>

- [<span data-ttu-id="82044-128">Acerca del modelo de seguridad de las plantillas de formulario con código</span><span class="sxs-lookup"><span data-stu-id="82044-128">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)
- [<span data-ttu-id="82044-129">Implementar plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="82044-129">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
- [<span data-ttu-id="82044-130">Controlar los errores con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="82044-130">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [<span data-ttu-id="82044-131">Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza</span><span class="sxs-lookup"><span data-stu-id="82044-131">Preview and Debug Form Templates that Require Full Trust</span></span>](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [<span data-ttu-id="82044-132">Depurar proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="82044-132">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
