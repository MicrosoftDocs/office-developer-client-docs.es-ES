---
title: Implementar plantillas de formulario de InfoPath con código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- deploying form templates [infopath 2007],InfoPath 2007, deploying form templates,form templates [InfoPath 2007], deploying,.NET Framework security settings [InfoPath 2007],deployment [InfoPath 2007], form templates
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: El código de formulario para una plantilla de formulario con código administrado de InfoPath se compila como un ensamblado que se ejecuta en Common Language Runtime (CLR). Esto significa que, cada vez que se llevan a cabo modificaciones en el código de formulario, es necesario abrir el proyecto en Visual Studio 2012, realizar los cambios en el editor de código, volver a compilar la plantilla de formulario y, después, volver a implementar la plantilla de formulario. Asimismo, puesto que el ensamblado privado de una plantilla de formulario con código administrado se ejecuta en el dominio de una aplicación CLR hospedada, la configuración de seguridad de los formularios que requieren plena confianza es algo diferente de las plantillas de formulario que no requieren plena confianza.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406902"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Implementar plantillas de formulario de InfoPath con código

El código de formulario para una plantilla de formulario con código administrado de InfoPath se compila como un ensamblado que se ejecuta en Common Language Runtime (CLR). Esto significa que, cada vez que se llevan a cabo modificaciones en el código de formulario, es necesario abrir el proyecto en Visual Studio 2012, realizar los cambios en el editor de código, volver a compilar la plantilla de formulario y, después, volver a implementar la plantilla de formulario. Asimismo, puesto que el ensamblado privado de una plantilla de formulario con código administrado se ejecuta en el dominio de una aplicación CLR hospedada, la configuración de seguridad de los formularios que requieren plena confianza es algo diferente de las plantillas de formulario que no requieren plena confianza.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Implementar plantillas de formulario que no requieren plena confianza

Si el código de la plantilla de formulario no utiliza miembros del modelo de objetos de InfoPath ni características que requieran plena confianza, es posible publicarla directamente desde InfoPath siguiendo este procedimiento. Para obtener información sobre el modelo de seguridad de InfoPath, vea [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Implementar una plantilla de formulario que no requiera plena confianza

1. Cree y depure la plantilla de formulario en Visual Studio 2012.
    
2. Si trabaja en el editor de código de Visual Studio 2012, cambie a InfoPath, haga clic en la pestaña **Archivo** y, a continuación, haga clic en el botón para la ubicación de publicación deseada en la ficha **Publicar**. (Si ya publicó la plantilla de formulario anteriormente, puede hacer clic en la pestaña **Archivo** y después elegir **Publicación rápida** para volver a publicar la plantilla de formulario en la misma ubicación). 
    
    La plantilla de formulario se compila y se inicia el **Asistente para la publicación**. Siga los pasos del **Asistente para la publicación** para implementar el formulario en una ubicación de su elección. Para obtener más información sobre el uso del **Asistente para la publicación**, busque el tema sobre la publicación de una plantilla de formulario en la Ayuda de InfoPath.
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Implementar plantillas de formulario que requieren plena confianza

Si el código de formulario de la plantilla de formulario utiliza miembros del modelo de objetos de InfoPath que requieren plena confianza o la plantilla de formulario utiliza características que requieren plena confianza, debe firmar digitalmente el archivo de plantilla de formulario (.xsn) utilizando un certificado de firma de código procedente de un editor de confianza. Al abrir el formulario, se preguntará a los usuarios si confían en el certificado. Además, con ello se logrará que el formulario sea de plena confianza y que se le conceda el conjunto de permisos de plena confianza al código de éste.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Compilar, publicar y firmar digitalmente una plantilla de formulario

1. Cree y depure la plantilla de formulario en Visual Studio 2012.
    
2. Si trabaja en el editor de código de Visual Studio 2012, cambie a InfoPath, haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario**.
    
3. Haga clic en la categoría **Seguridad y confianza**. 
    
4. En **Nivel de seguridad**, desactive la casilla **Determinar automáticamente el nivel de seguridad** y después seleccione **Plena confianza**.
    
5. En **Firma de plantillas de formulario**, seleccione **Firmar esta plantilla de formulario**, haga clic en **Seleccionar certificado** y especifique el certificado de firma de código con el que firmar la plantilla de formulario.
    
6. Haga clic en **Aceptar** dos veces para cerrar el cuadro de diálogo **Opciones de formulario** y, a continuación, guarde los cambios. 
    
7. Haga clic en la pestaña **Publicar** y a continuación haga clic en el botón de la ubicación de publicación deseada. 
    
8. La plantilla de formulario se compila y se inicia el **Asistente para la publicación**. Siga los pasos del **Asistente para la publicación** para implementar la plantilla de formulario en una ubicación de su elección. Para obtener más información sobre el uso del **Asistente para la publicación** para implementar una plantilla de formulario que requiere plena confianza, busque en la Ayuda de InfoPath "Publicar una plantilla de formulario con plena confianza". 
    
 **Notas**
- Para firmar digitalmente un formulario, debe tener instalado en el equipo un certificado de firma de código autenticado. Para adquirir este certificado, se deberá poner en contacto con un una entidad emisora de certificados o el administrador de la red.
    
- Si necesita realizar cambios en el formulario después de la publicación, debe repetir el procedimiento y volver a firmar la plantilla de formulario. Esto se debe a que la modificación del formulario invalida la firma digital. Durante el desarrollo de un formulario que requiere permisos de [](how-to-preview-and-debug-form-templates-that-require-full-trust.md) plena confianza, puede usar el procedimiento descrito en Vista previa y Depurar plantillas de formulario que requieren plena confianza para registrar la plantilla de formulario en el equipo local. 
    
## <a name="configuring-net-framework-security-settings"></a>Configurar las opciones de seguridad de .NET Framework

Para tener más control sobre los permisos que se conceden para ejecutar código administrado en una plantilla de formulario de InfoPath con código administrado, use la utilidad de configuración .NET Framework 2.0 para conceder un conjunto de permisos concreto al código del formulario.
  
> [!IMPORTANT]
> [!IMPORTANTE] La configuración de opciones de seguridad de .NET Framework para una plantilla de formulario con código administrado de InfoPath no afecta a la capacidad de ejecutar los miembros del modelo de objetos de InfoPath que requieren plena confianza. Debe firmar digitalmente o registrar las plantillas de formulario de la forma descrita anteriormente en este tema para habilitar las llamadas a los miembros del modelo de objetos de InfoPath que requieran plena confianza. La configuración de las opciones de seguridad de .NET Framework se aplica solo a las llamadas a miembros de las clases de .NET Framework y a los componentes administrados que sean distintos del modelo de objetos de InfoPath. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Compilar, publicar y configurar las opciones de seguridad de .NET para una plantilla de formulario

1. Cree y depure la plantilla de formulario en Visual Studio 2012.
    
2. Si trabaja en el editor de código de Visual Studio 2012, cambie a InfoPath, haga clic en la pestaña **Archivo**, haga clic en **Publicar** y a continuación haga clic en el botón de la ubicación de publicación deseada.
    
    La plantilla de formulario se compila y se inicia el **Asistente para la publicación**. Siga los pasos del **Asistente para la publicación** para implementar la plantilla de formulario. Para obtener más información sobre el uso del **Asistente para la publicación**, busque el tema "Publicar una plantilla de formulario" en la Ayuda de InfoPath.
    
3. Realice el procedimiento descrito en la sección "Asignación de plena confianza a formularios en una dirección URL específica o UNC" de la sección Configurar opciones de seguridad para plantillas de [formulario con código](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Vea también

#### <a name="tasks"></a>Tareas

[Configuración de la seguridad de las plantillas de formulario con código](how-to-configure-security-settings-for-form-templates-with-code.md)


[Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
  
[Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

