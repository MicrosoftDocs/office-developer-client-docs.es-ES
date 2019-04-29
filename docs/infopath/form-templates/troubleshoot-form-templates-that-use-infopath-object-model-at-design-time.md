---
title: Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de diseño
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- plantillas de formulario compatibles con InfoPath 2003, solución de problemas en tiempo de diseño, solución de problemas de plantillas de formulario [InfoPath 2007], tiempo de diseño
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se diseñan y depuran plantillas de formulario de código administrado que usan el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: 106f12602bae86d85c2a7d2f920f59d50326c908
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436527"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de diseño

En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se diseñan y depuran plantillas de formulario de código administrado que usan el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust**. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>No se pueden depurar plantillas de formulario que utilizan llamadas a métodos y propiedades de nivel de seguridad 3 del modelo de objetos ni obtener una vista previa de las mismas

Si intenta depurar u obtener una vista previa de un proyecto de código administrado cuyo código invoque miembros del modelo de objetos que requieren plena confianza, InfoPath mostrará el mensaje de error "Excepción de seguridad no controlada en el código del formulario" y el formulario no se abrirá. Para permitir que la lógica empresarial de la plantilla de formulario se pueda depurar u obtener una vista previa de la misma, deberá establecer el nivel de seguridad en **Plena confianza** y firmar digitalmente la plantilla de formulario. Para obtener más información sobre cómo hacerlo, vea [vista previa y depuración de plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>No se pueden actualizar las expresiones XPath de los controladores de eventos si el valor del parámetro MatchPath se ha eliminado manualmente

Si agrega un controlador de eventos a un campo o grupo y, después, modifica el esquema del origen de datos en el panel de tareas **Campos** de InfoPath de una forma que afecte a ese campo o grupo (por ejemplo, cambiando su nombre o moviéndolo), aparecerá un mensaje que le preguntará si desea actualizar las expresiones XPath del código del formulario. Las expresiones de XPath a las que se hace referencia en este mensaje son los valores especificados en el parámetro [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) del atributo [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) , que se usan para asociar el controlador de eventos a un campo o grupo del origen de datos del formulario. . No se actualizará ninguna otra expresión XPath del código. El algoritmo para actualizar las expresiones XPath depende del valor que esté presente en el parámetro **MatchPath** de los atributos **InfoPathEventHandler** que se aplican al código del formulario. Si eliminó manualmente estos valores antes de responder a la pregunta sobre la actualización de las expresiones XPath, InfoPath no podrá actualizar las expresiones XPath automáticamente. Para obtener más información, vea [Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>No se puede llamar a miembros del modelo de objetos compatible con InfoPath 2003 en un subproceso separado

El modelo de objetos de InfoPath no admite las llamadas en un subproceso separado. Por ejemplo, el ejemplo de código siguiente, que llama a una función denominada LaunchOMFunction que a su vez llama a miembros del modelo de objetos de InfoPath, no se ejecutará. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

No obstante, si es necesario, existe una forma de superar esta limitación. Para obtener más información, vea [compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de infopath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>La omisión de parámetros opcionales da lugar a un error de generación en Visual Basic y Visual C#

Si un miembro del modelo de objetos de InfoPath contiene un parámetro opcional y no especifica un valor para ese parámetro, deberá pasar el campo **Type.Missing** de ese parámetro. Si no se pasa el campo **Type.Missing** al omitir un valor real, se producirá un error de generación. Esto es aplicable tanto al código escrito en Visual Basic como en Visual C#. Para obtener más información y ejemplos, vea la sección "pasar parámetros opcionales a los miembros del modelo de objetos de InfoPath" en el tema [modelos de objetos compatibles con infopath 2003](infopath-2003-compatible-object-models.md) . 
  
## <a name="see-also"></a>Ver también

- [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
- [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md)
- [Controlar errores con el modelo de objetos de InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [DePurar proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

