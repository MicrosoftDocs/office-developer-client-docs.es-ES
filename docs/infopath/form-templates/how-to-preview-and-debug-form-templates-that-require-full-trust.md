---
title: Vista previa y depuración de plantillas de formulario que requieren plena confianza
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: De manera predeterminada, si intenta depurar u obtener una vista previa de un proyecto de código administrado que tiene código que llama a un miembro del modelo de objetos que requiere plena confianza, como la propiedad LoginName que requiere acceso a la información sobre el dominio de inicio de sesión del usuario, Microsoft InfoPath mostrará los mensajes siguientes.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411263"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="5f03e-104">Vista previa y depuración de plantillas de formulario que requieren plena confianza</span><span class="sxs-lookup"><span data-stu-id="5f03e-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="5f03e-105">De manera predeterminada, si intenta depurar u obtener una vista previa de un proyecto de código administrado que tiene código que llama a un miembro del modelo de objetos que requiere plena confianza, como la propiedad **LoginName** que requiere acceso a la información sobre el dominio de inicio de sesión del usuario, Microsoft InfoPath mostrará los mensajes siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f03e-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="5f03e-106">Durante la vista previa:</span><span class="sxs-lookup"><span data-stu-id="5f03e-106">When previewing:</span></span>
  
<span data-ttu-id="5f03e-p101">"Tuvo lugar una excepción no controlada en el código del formulario", seguido de "InfoPath no puede completar esta acción debido a un error en el código del formulario".</span><span class="sxs-lookup"><span data-stu-id="5f03e-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="5f03e-109">Durante la depuración:</span><span class="sxs-lookup"><span data-stu-id="5f03e-109">When debugging:</span></span>
  
<span data-ttu-id="5f03e-110">El foco se desplazará a la línea de código en el editor de código que está llamando al miembro que requiere plena confianza; se mostrará el mensaje siguiente: "El código de usuario no controló **SecurityException** - Error de la solicitud".</span><span class="sxs-lookup"><span data-stu-id="5f03e-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="5f03e-111">Para permitir que la lógica empresarial llame a este miembro cuando se está depurando o durante la vista previa, debe configurar el nivel de seguridad de la plantilla en **Plena confianza**, como se describe en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f03e-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="5f03e-112">Configuración de una plantilla de formulario de código administrado que requiera plena confianza</span><span class="sxs-lookup"><span data-stu-id="5f03e-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="5f03e-113">Establecer el nivel de seguridad del formulario en Plena confianza</span><span class="sxs-lookup"><span data-stu-id="5f03e-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="5f03e-114">En InfoPath, abra la plantilla de formulario en el modo de diseño.</span><span class="sxs-lookup"><span data-stu-id="5f03e-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="5f03e-115">Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**.</span><span class="sxs-lookup"><span data-stu-id="5f03e-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="5f03e-116">En la lista **Categoría**, haga clic en **Seguridad y confianza**</span><span class="sxs-lookup"><span data-stu-id="5f03e-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="5f03e-117">En **Nivel de seguridad**, desactive la casilla **Determinar automáticamente el nivel de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="5f03e-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="5f03e-118">Seleccione **Plena confianza** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5f03e-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="5f03e-119">Una vez realizado este procedimiento, puede depurar el proyecto tal como se describe en Vista previa y depurar plantillas de formulario de [InfoPath con código.](how-to-preview-and-debug-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="5f03e-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5f03e-120">[!NOTA] Para implementar correctamente una plantilla de formulario con código administrado que requiera plena confianza, hay que llevar a cabo unos pasos adicionales, como una firma digital o instalar y registrar la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="5f03e-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="5f03e-121">Para obtener información sobre cómo implementar una plantilla de formulario con código administrado después de depurarla, vea Implementar plantillas de formulario de [InfoPath con código.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="5f03e-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f03e-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f03e-122">See also</span></span>



[<span data-ttu-id="5f03e-123">Obtener una vista previa y depurar plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="5f03e-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="5f03e-124">Implementar plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="5f03e-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

