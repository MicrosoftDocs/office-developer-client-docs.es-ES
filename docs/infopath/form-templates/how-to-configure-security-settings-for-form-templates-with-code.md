---
title: Configurar las opciones de seguridad de las plantillas de formulario con código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Puede personalizar el conjunto de permisos que se aplicará a las plantillas de formulario de código administrado de InfoPath usando el complemento Configuración de .NET.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300169"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Configurar las opciones de seguridad de las plantillas de formulario con código

Puede personalizar el conjunto de permisos que se aplicará a las plantillas de formulario de código administrado de InfoPath usando el complemento Configuración de .NET.
  
El componente CLR que hospeda InfoPath buscará un grupo de código predefinido denominado  *Plantillas de formulario de InfoPath*  en el grupo Todo_el_código del nivel de directivas Equipo. CLR aplicará los conjuntos de permisos definidos en ese grupo al dominio de aplicación (AppDomain) en el que se ejecuta el código. Ello permite personalizar los conjuntos de permisos que se conceden a las plantillas de formulario con código administrado de InfoPath. Por ejemplo, puede conceder permiso para obtener acceso a Active Directory a plantillas de formulario descargadas desde https://MySite. 
  
Para que la directiva de seguridad personalizada definida mediante el complemento Configuración de .NET se aplique, se debe implementar en todos los equipos cliente en los que se vaya a ejecutar la plantilla de formularios.
  
Para obtener más información sobre el modelo de seguridad de las plantillas de formulario con código administrado de InfoPath, vea [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Crear un grupo de código para las plantillas de formulario de InfoPath

En el procedimiento siguiente se crea un grupo de código que no concede permisos a plantillas de formulario con código administrado de InfoPath (excepto las que están instaladas o registradas en el equipo local), en el que puede asignar grupos de permisos a plantillas de formulario de InfoPath ubicadas en direcciones URL o UNC específicas. Para obtener más información sobre cómo crear y asignar grupos de código dentro del grupo de código  `InfoPath Form Templates`, vea el procedimiento siguiente. 
  
> [!NOTE]
> [!NOTA] A diferencia de la herramienta **Configuración de Microsoft .NET Framework 1.1** que se instala con Microsoft .NET Framework 1.1 Redistributable Package, **Configuración de Microsoft .NET Framework 2.0** se instala sólo con Microsoft .NET Framework 2.0 Software Development Kit (SDK). 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>Creación de un grupo de código de seguridad personalizado para los formularios con código administrado de InfoPath

1. En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.
    
    Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.
    
2. En **Mi PC**, expanda los nodos **Directiva de seguridad en tiempo de ejecución**, **Equipo**, **Grupos de código**, **Todo_el_código**; a continuación, haga clic con el botón secundario en el nodo **Todo_el_código** y, por último, haga clic en **Nuevo** para abrir el cuadro de diálogo **Crear grupo de código**. 
    
3. Escriba el nuevo grupo de código  `InfoPath Form Templates` (escriba el texto exactamente) y haga clic en **Siguiente**.
    
4. Establezca el tipo de condición del grupo de código en **Todo el código** y, a continuación, haga clic en **Siguiente**.
    
5. Haga clic en **Usar el conjunto de permisos existente**, asigne el conjunto de permisos **Nada** al grupo de código, haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar**.
    
6. Para aplicar la nueva configuración, cierre y reinicie InfoPath.
    
Si lo prefiere, puede administrar el conjunto de permisos de todas las plantillas de formulario con código administrado de InfoPath asignando un conjunto de permisos que no sea **Nada** al grupo de código **Plantillas de formulario de InfoPath**. 
> [!NOTE]
> [!NOTA] Puede cambiar el conjunto de permisos de un grupo de código de seguridad en cualquier momento. Para ello, abra el complemento **Configuración de .NET 2,0**, haga clic con el botón secundario en el grupo, haga clic en **Propiedades** y, a continuación, en la pestaña **Conjunto de permisos**. 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Asignar el conjunto de permisos Plena confianza a los formularios de una dirección URL o UNC específica

Puede crear grupos de código en el grupo **Plantillas de formulario de InfoPath** para conceder el conjunto de permisos de plena confianza a las plantillas de una ubicación URL o UNC concreta. Una vez realizada esta operación, se ejecutarán como plantillas de formulario de plena confianza todas las que se publiquen en la ubicación especificada. 
  
> [!NOTE]
> [!NOTA] InfoPath carga las plantillas de formulario del equipo local (grupo de código Zona Mi PC) usando una dirección URL aleatoria. Por esta razón, no se puede usar el procedimiento que se describe a continuación para conceder el conjunto de permisos FullTrust a estas plantillas de formularios. Para conceder una plantilla de formulario instalada de forma local al conjunto de permisos FullTrust, use uno de los procedimientos que se describen en la sección "implementación de plantillas de formulario que requieren plena confianza" del tema [implementación de plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md) . 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>Asignar el conjunto de permisos FullTrust a formularios de InfoPath que se encuentran en una ubicación URL o UNC específica

1. En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.
    
    Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.
    
2. En **Mi PC**, expanda los nodos **Directiva de seguridad en tiempo de ejecución**, **Equipo**, **Grupos de código**, **Todo_el_código** y, a continuación, haga clic en el nodo **Plantillas de formulario de InfoPath**. 
    
3. En la lista **Tareas** del panel derecho, haga clic en **Agregar un grupo de código secundario**, escriba un nombre para el grupo de código y, a continuación, haga clic en **Siguiente**.
    
4. En la lista **Elija el tipo de condición para este grupo de códigos**, seleccione **URL** y, a continuación, escriba la dirección URL o UNC de la ubicación de las plantillas de formulario con código administrado de InfoPath a las que desea conceder el conjunto de permisos **Plena confianza**. 
    
    Para restringir el conjunto de permisos a una única plantilla de formularios, especifique la ruta de acceso completa de ésta. Por ejemplo:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Para conceder el conjunto de permisos a todas las plantillas de formulario de una dirección URL o UNC, omita el nombre de la plantilla y agregue un asterisco al final de la dirección URL o UNC. Por ejemplo:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Haga clic en **Siguiente**, a continuación, en **Usar el conjunto de permisos existente** y asigne el conjunto de permisos **Plena confianza** al grupo de código. 
    
6. Haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar**.
    
7. Para aplicar la nueva configuración, cierre y reinicie InfoPath.
    
> [!NOTE]
> [!NOTA] Para aplicar un conjunto de permisos personalizado o más restrictivo, seleccione la opción más apropiada, en lugar de **Plena confianza**, en el paso 4. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Creación de un paquete de implementación para la directiva de seguridad de InfoPath

Una vez definida la directiva de seguridad personalizada para las plantillas de formulario administradas de InfoPath puede crear un paquete Windows Installer (.msi) para implementar esta directiva de seguridad en los equipos de los usuarios usando la directiva de grupo o Microsoft Systems Management Server.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>Crear un paquete de implementación para la directiva de seguridad de InfoPath

1. En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.
    
    Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.
    
2. Haga clic con el botón secundario en **Directiva de seguridad en tiempo de ejecución** y, a continuación, haga clic en **Crear paquete de implementación**.
    
3. En **Seleccione el nivel de directiva de seguridad que desea implementar**, haga clic en **Equipo**, especifique la carpeta y el nombre de archivo para el paquete Windows Installer y, a continuación, haga clic en **Siguiente**.
    
4. Haga clic en **Finalizar** para crear el paquete de implementación. 
    
5. Para obtener información sobre cómo usar la herramienta de configuración de .NET Framework, busque "herramienta de configuración de .NET Framework (Mscorcfg. msc)" en la ayuda de Visual Studio o en el sitio web de MSDN.
    
## <a name="see-also"></a>Vea también



[Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)

