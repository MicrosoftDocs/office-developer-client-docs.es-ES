---
title: Agregar un controlador de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched event [InfoPath 2007],event handling [InfoPath 2007],Merge event [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007],Loading event [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: En este tema se describen los procedimientos para agregar controladores de eventos a una plantilla de formulario con código administrado de Microsoft InfoPath mediante Visual Studio 2012. Para agregar un controlador de eventos a una plantilla de formulario, comience con la plantilla de formulario abierta en InfoPath Designer y, a continuación, seleccione el comando de interfaz de usuario adecuado para el evento para el que desea escribir código. Después de seleccionar el comando para un evento en InfoPath Designer, el foco cambia automáticamente al esqueleto del controlador de eventos para ese evento en el editor de código de Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427188"
---
# <a name="add-an-event-handler"></a>Agregar un controlador de eventos

En este tema se describen los procedimientos para agregar controladores de eventos a una plantilla de formulario con código administrado de Microsoft InfoPath mediante Visual Studio 2012. Para agregar un controlador de eventos a una plantilla de formulario, comience con la plantilla de formulario abierta en InfoPath Designer y, a continuación, seleccione el comando de interfaz de usuario adecuado para el evento para el que desea escribir código. Después de seleccionar el comando para un evento en InfoPath Designer, el foco cambia automáticamente al esqueleto del controlador de eventos para ese evento en el editor de código de Visual Studio 2012.
  
> [!IMPORTANT]
> Siempre debe usar la interfaz de usuario de InfoPath Designer para agregar un controlador de eventos. Al agregar un controlador de eventos con la interfaz de usuario, se genera un código de enlace de eventos en el método **InternalStartup** del archivo FormCode.cs o FormCode.vb en el proyecto de plantilla de formulario. No cree el método **InternalStartup** ni le agregue código adicional. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Agregar un controlador de eventos para el evento Click de un control Button

1. Abra la plantilla de formulario en InfoPath Designer y, a continuación, agregue un control **Button** al formulario. 
    
2. Haga clic en el botón y, a continuación, en la ficha **Propiedades** de la cinta, haga clic en **Código personalizado**.
    
    El foco se desplazará al esqueleto del controlador de eventos del evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) en el editor de código de Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Agregar un controlador de eventos para el evento Changing, Validating o Changed de un campo o un grupo

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. Haga clic con el botón secundario en un control de entrada de datos enlazado al campo o grupo, como un control de **Cuadro de texto**. 
    
3. Elija **Programación** y haga clic en el evento para el que desea crear un controlador de eventos. El foco se desplazará al esqueleto del controlador de eventos del evento [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) o [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) en el editor de código de Visual Studio 2012. 
    
    > [!NOTE]
    > [!NOTA] El comando para crear un controlador de eventos para el evento **Changing** no está disponible si la configuración de compatibilidad de la plantilla de formulario está establecida en **Formulario de explorador web**. Esto se debe a que el evento **Changing** no es compatible con la lógica empresarial de las plantillas de formulario que se publican en las bibliotecas de documentos de Microsoft SharePoint Server 2010 con InfoPath Forms Services. Para crear un controlador de eventos para el evento **Changing**, debe cambiar la configuración de compatibilidad a **InfoPath Editor** en InfoPath Designer. Para esto, haga clic en la pestaña **Archivo**, haga clic en **Opciones de formulario**, haga clic en **Compatibilidad** y establezca **Tipo de formulario** en **Formulario de InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Agregar un controlador de eventos para los eventos Loading, ViewSwitched, ContextChanged y Sign de un formulario

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. En la ficha **Programador** de la cinta, haga clic en el evento de formulario para el que desee escribir un controlador de eventos. 
    
    El foco se desplazará al esqueleto de controlador de eventos del evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) o [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) en el editor de código de Visual Studio 2012. 
    
    > [!NOTE]
    > [!NOTA] Los comandos para crear un controlador de eventos para los eventos [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) o [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) no están disponibles si la configuración de compatibilidad de la plantilla de formulario está establecida en **Formulario de explorador web**. Esto se debe a que tales eventos no se admiten en la lógica empresarial de las plantillas de formulario que se publican en bibliotecas de documentos de Microsoft SharePoint Server 2010 con InfoPath Forms Services. Para crear un controlador de eventos para el evento [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) o [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) debe cambiar la configuración de compatibilidad a **Formulario de InfoPath Editor** en InfoPath Designer. Para esto, haga clic en la pestaña **Archivo**, haga clic en **Opciones de formulario**, haga clic en **Compatibilidad** y establezca **Tipo de formulario** en **Formulario de InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Agregar un controlador de eventos para el evento Submit de un formulario

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo**, haga clic en **Enviar a** en la ficha **Información** y, a continuación, haga clic en ** Opciones de envío **.
    
3. Haga clic en **Permitir a los usuarios enviar este formulario**, a continuación en **Realizar una acción personalizada utilizando código** y, por último, haga clic en **Modificar código**.
    
    Se desplazará el foco al esqueleto del controlador de eventos del evento [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) en el editor de código de Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Agregar un controlador de eventos para el evento Save de un formulario

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. Haga clic en la categoría **Guardar**, active la casilla de verificación **Guardar usando código personalizado** y después haga clic en **Editar**.
    
    Se desplazará el foco al esqueleto del controlador de eventos del evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) en el editor de código de Visual Studio 2012. 
    
    > [!NOTE]
    > [!NOTA] La casilla de verificación **Guardar usando código personalizado** no está disponible si la configuración de compatibilidad de la plantilla de formulario es **InfoPath Forms Services**. Esto se debe a que el evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no se admite en la lógica empresarial de las plantillas de formulario publicadas en las bibliotecas de documentos de Microsoft SharePoint Server 2010 con InfoPath Forms Services. Para crear un controlador de eventos para el evento [Save,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) debe cambiar la configuración de compatibilidad a **Formulario de InfoPath Editor** en InfoPath Designer. Para esto, haga clic en la pestaña **Archivo**, haga clic en **Opciones de formulario**, haga clic en **Compatibilidad** y establezca **Tipo de formulario** en **Formulario de InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Agregar un controlador de eventos para el evento VersionUpgrade de un formulario

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. Haga clic en la categoría **Control de versiones**, seleccione **Utilizar evento personalizado** en el cuadro de lista desplegable **Actualizar formularios existentes** y haga clic en **Editar**.
    
    Se desplazará el foco al esqueleto del controlador de eventos del evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) en el editor de código de Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Agregar un controlador de eventos para el evento Merge de un formulario

1. Abra la plantilla de formulario en InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. En la categoría **Avanzadas**, haga clic en la casilla de verificación **Habilitar la combinación de formularios**, active la casilla de verificación **Combinar usando código personalizado** y haga clic en **Editar**.
    
    Se desplazará el foco al esqueleto del controlador de eventos del evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) en el editor de código de Visual Studio 2012. 
    
    > [!NOTE]
    > [!NOTA] La casilla de verificación **Habilitar la combinación de formularios** no está disponible si la configuración de compatibilidad de la plantilla de formulario está establecida en **InfoPath Forms Services**. Esto se debe a que el evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) no se admite en la lógica empresarial de las plantillas de formulario publicadas en las bibliotecas de documentos de Microsoft SharePoint Server 2010 con InfoPath Forms Services. Para crear un controlador de eventos para el evento [Merge,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) debe cambiar la configuración de compatibilidad a **Formulario de InfoPath Editor** en InfoPath Designer. Para esto, haga clic en la pestaña **Archivo**, haga clic en **Opciones de formulario**, haga clic en **Compatibilidad** y establezca **Tipo de formulario** en **Formulario de InfoPath Editor**. 
  
## <a name="see-also"></a>Consulte también



[Tutorial: Crear una plantilla de formulario básica con código](walkthrough-creating-a-basic-form-template-with-code.md)

