---
title: Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: De manera predeterminada, si intenta depurar u obtener una vista previa de un proyecto de código administrado que tiene código que llama a un miembro del modelo de objetos que requiere plena confianza, como la propiedad LoginName que requiere acceso a la información sobre el dominio de inicio de sesión del usuario, Microsoft InfoPath mostrará los mensajes siguientes.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815864"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza

De manera predeterminada, si intenta depurar u obtener una vista previa de un proyecto de código administrado que tiene código que llama a un miembro del modelo de objetos que requiere plena confianza, como la propiedad **LoginName** que requiere acceso a la información sobre el dominio de inicio de sesión del usuario, Microsoft InfoPath mostrará los mensajes siguientes. 
  
Durante la vista previa:
  
"Tuvo lugar una excepción no controlada en el código del formulario", seguido de "InfoPath no puede completar esta acción debido a un error en el código del formulario".
  
Durante la depuración:
  
El foco se desplazará a la línea de código en el editor de código que está llamando al miembro que requiere plena confianza; se mostrará el mensaje siguiente: "El código de usuario no controló **SecurityException** - Error de la solicitud". 
  
Para permitir que la lógica empresarial llame a este miembro cuando se está depurando o durante la vista previa, debe configurar el nivel de seguridad de la plantilla en **Plena confianza**, como se describe en el procedimiento siguiente. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Configuración de una plantilla de formulario de código administrado que requiera plena confianza

### <a name="set-your-forms-security-level-to-full-trust"></a>Establecer el nivel de seguridad del formulario en Plena confianza

1. En InfoPath, abra la plantilla de formulario en el modo de diseño.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. En la lista **Categoría**, haga clic en **Seguridad y confianza**
    
4. En **Nivel de seguridad**, desactive la casilla **Determinar automáticamente el nivel de seguridad**.
    
5. Seleccione **Plena confianza** y, a continuación, haga clic en **Aceptar**.
    
Después de que se lleva a cabo este procedimiento, puede depurar el proyecto, como se describe en la [vista previa y depurar plantillas de formulario de InfoPath con código](how-to-preview-and-debug-infopath-form-templates-with-code.md).
  
> [!NOTE]
> [!NOTA] Para implementar correctamente una plantilla de formulario con código administrado que requiera plena confianza, hay que llevar a cabo unos pasos adicionales, como una firma digital o instalar y registrar la plantilla de formulario. Para obtener información sobre la implementación de una plantilla de formulario de código administrado después de que se está depurando, consulte [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Vea también



[Obtener una vista previa y depurar plantillas de formulario de InfoPath con código](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md)

