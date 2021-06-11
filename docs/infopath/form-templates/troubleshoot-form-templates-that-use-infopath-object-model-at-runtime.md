---
title: Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de ejecución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solución de problemas de plantillas de formulario [infopath 2007], tiempo de ejecución, plantillas de formulario compatibles con InfoPath 2003, solución de problemas en tiempo de ejecución
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: En las secciones siguientes se describen escenarios comunes de solución de problemas que puede encontrar al trabajar con plantillas de formulario de código administrado de InfoPath que usan el modelo de objetos compatible con InfoPath 2003 proporcionado por Microsoft. Office.Interop.InfoPath.SemiTrust espacio de nombres en tiempo de ejecución.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414448"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de ejecución

En las secciones siguientes se describen escenarios comunes de solución de problemas que puede encontrar al trabajar con plantillas de formulario de código administrado de InfoPath que usan el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** en tiempo de ejecución. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Mostrar notificaciones para excepciones de código administrado no controladas en tiempo de ejecución

Si no utiliza el control de las excepciones try-catch en el código del formulario, InfoPath mostrará información sobre las excepciones no controladas en el cuadro de diálogo de errores de InfoPath mientras se depuran y se obtiene una vista previa. No obstante, de manera predeterminada, dichas excepciones no se muestran en el cuadro de diálogo de errores de InfoPath en tiempo de ejecución al implementar una plantilla de formulario con código administrado. Si desea que se muestren excepciones de código administrado en tiempo de ejecución, siga el procedimiento de la sección "Control de excepciones de código administrado" de Controlar errores mediante el modelo de objetos de [InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problemas con plantillas de formulario de código administrado después de la implementación

Asegúrese de que prueba las plantillas de formulario con código administrado en la ubicación en la que se van a implementar finalmente. Para obtener información sobre los procedimientos de implementación, vea [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md). Para obtener información sobre los escenarios de seguridad que afectan a la implementación, vea [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md).
  
Si usa la utilidad de configuración de .NET Framework 1.1 y el grupo de código de las plantillas de formulario de InfoPath para agregar permisos específicos a una plantilla de formulario con código administrado, asegúrese de que implementa la misma directiva de seguridad en todos los equipos cliente. Además, si especifica una **URLEvidence** que se refiere a una ubicación del equipo local, asegúrese de que ésta sea la de la carpeta en la que se implementará finalmente la solución (que no sea la misma ubicación utilizada durante el desarrollo). Para obtener información sobre cómo configurar la configuración de seguridad de .NET Framework para una plantilla de formulario de código administrado, vea la sección "Asignación de FullTrust a formularios en una dirección URL específica o UNC" del tema [Configure Security Configuración for Form Templates with Code.](how-to-configure-security-settings-for-form-templates-with-code.md) 
  
## <a name="see-also"></a>Vea también

- [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
- [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md)
- [Controlar errores mediante el modelo de objetos de InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Depurar proyectos de InfoPath con el modelo de objetos de InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

