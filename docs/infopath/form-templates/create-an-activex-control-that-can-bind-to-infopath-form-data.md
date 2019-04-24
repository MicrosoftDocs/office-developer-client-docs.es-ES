---
title: Crear un control ActiveX que pueda enlazar a datos de formulario de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Se pueden hospedar controles ActiveX en formularios de InfoPath diseñados para abrirse en el editor de InfoPath. Estos controles pueden existir previamente (con algunas restricciones) o escribirse específicamente para InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300192"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Crear un control ActiveX que pueda enlazar a datos de formulario de InfoPath

Se pueden hospedar controles ActiveX en formularios de InfoPath diseñados para abrirse en el editor de InfoPath. Estos controles pueden existir previamente (con algunas restricciones) o escribirse específicamente para InfoPath.
  
## <a name="write-an-activex-control"></a>Escribir un control ActiveX

Tal como ocurre con otros controles en InfoPath, los controles ActiveX deben ser compatibles con las interfaces existentes del Modelo de objetos componentes (COM):
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Para que InfoPath actualice las propiedades del Modelo de objetos de documentos (DOM) en el momento en que cambian en el control, el control debe implementar las interfaces siguientes:
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
Asimismo, existen dos interfaces COM específicas de InfoPath que permiten una mejor integración de controles:
  
- [IInfoPathControl](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [IInfoPathControlSite](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Agregar un control ActiveX al entorno de diseño de InfoPath

El comando **Agregar o quitar controles personalizados** en el panel de tareas **Controles** permite usar el **Asistente para agregar un control personalizado** para agregar un control personalizado. Al usar el asistente, se puede seleccionar un control ActiveX que ya se haya registrado o buscar otros controles personalizados en el Catálogo de soluciones de Office. Después de seleccionar un control, se pueden especificar los siguientes elementos. 
  
- Especificar un archivo CAB para instalar el control ActiveX con la plantilla de formulario.
    
- Especificar una propiedad de enlace para enlazar al XML.
    
- Especificar una propiedad que se use para habilitar o deshabilitar el control en respuesta a las reglas o firmas digitales, lo cual puede resultar útil, por ejemplo, cuando el XML no está presente o cuando se usa formato condicional.
    
- Especificar el enlace del tipo de datos.
    
> [!NOTE]
> [!NOTA] Si está desarrollando un control ActiveX y lo agrega al panel de tareas **Controles** de InfoPath, no se podrá volver a generar el control ActiveX hasta que se cierre InfoPath. 
  
## <a name="deploy-an-activex-control"></a>Implementar un Control ActiveX

Para distribuir un control ActiveX, es posible escribir un instalador que instale el control en el equipo de destino y copie el archivo de Plantilla de control (ICT) de InfoPath y el archivo CAB en la carpeta del usuario, \Users\\<nombreUsuario\>\AppData\Local\Microsoft\InfoPath\Controls. Se debe tener en cuenta que si hay dos o más programadores que colaboran en el desarrollo de formularios que usan controles ActiveX, cada programador debe tener los controles que se agregaron al entorno de desarrollo de InfoPath, o no podrán modificar las propiedades de los controles desde InfoPath.
  
## <a name="see-also"></a>Vea también

Práctica 6: Agregar controles ActiveX en InfoPath 2003
  
[Crear un control personalizado de InfoPath con C# y .NET (Blog del equipo de InfoPath)](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

