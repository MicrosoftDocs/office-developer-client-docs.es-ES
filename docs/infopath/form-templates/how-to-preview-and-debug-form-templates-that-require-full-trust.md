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
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Vista previa y depuración de plantillas de formulario que requieren plena confianza

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
    
Una vez realizado este procedimiento, puede depurar el proyecto tal como se describe en Vista previa y depurar plantillas de formulario de [InfoPath con código.](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
> [!NOTE]
> [!NOTA] Para implementar correctamente una plantilla de formulario con código administrado que requiera plena confianza, hay que llevar a cabo unos pasos adicionales, como una firma digital o instalar y registrar la plantilla de formulario. Para obtener información sobre cómo implementar una plantilla de formulario con código administrado después de depurarla, vea Implementar plantillas de formulario de [InfoPath con código.](how-to-deploy-infopath-form-templates-with-code.md) 
  
## <a name="see-also"></a>Consulte también



[Obtener una vista previa y depurar plantillas de formulario de InfoPath con código](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md)

