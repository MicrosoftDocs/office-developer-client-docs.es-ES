---
title: Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de ejecución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se trabaja con plantillas de formulario con código administrado de InfoPath que usan el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust en tiempo de ejecución.
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815976"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Solucionar problemas de plantillas de formulario que usan el modelo de objetos de InfoPath en tiempo de ejecución

En las secciones siguientes, se describen situaciones habituales de solución de problemas que se pueden presentar cuando se trabaja con plantillas de formulario con código administrado de InfoPath que usan el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** en tiempo de ejecución. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Mostrar notificaciones de excepciones de código administrado no controladas en tiempo de ejecución

Si no utiliza el control de las excepciones try-catch en el código del formulario, InfoPath mostrará información sobre las excepciones no controladas en el cuadro de diálogo de errores de InfoPath mientras se depuran y se obtiene una vista previa. No obstante, de manera predeterminada, dichas excepciones no se muestran en el cuadro de diálogo de errores de InfoPath en tiempo de ejecución al implementar una plantilla de formulario con código administrado. Si desea que las excepciones de código administrado que se muestra en tiempo de ejecución, siga el procedimiento descrito en la sección "Controlar excepciones de código administrado" de [Controlar errores utilizando el modelo de objetos de InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problemas con las plantillas de formulario con código administrado después de la implementación

Asegúrese de que prueba las plantillas de formulario con código administrado en la ubicación en la que se van a implementar finalmente. Para obtener información sobre los procedimientos de implementación, vea [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md). Para obtener información sobre los escenarios de seguridad que afectan a la implementación, consulte el tema [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md).
  
Si usa la utilidad de configuración de .NET Framework 1.1 y el grupo de código de las plantillas de formulario de InfoPath para agregar permisos específicos a una plantilla de formulario con código administrado, asegúrese de que implementa la misma directiva de seguridad en todos los equipos cliente. Además, si especifica una **URLEvidence** que se refiere a una ubicación del equipo local, asegúrese de que ésta sea la de la carpeta en la que se implementará finalmente la solución (que no sea la misma ubicación utilizada durante el desarrollo). Para obtener información acerca de cómo configurar la configuración de seguridad de .NET Framework para una plantilla de formulario con código administrado, vea la sección "Asignar FullTrust a formularios en un específico dirección URL o UNC" del tema [Configurar opciones de seguridad para las plantillas de formulario con código](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Vea también

- [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
- [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md)
- [Controlar los errores con el modelo de objetos de InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Depurar proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

