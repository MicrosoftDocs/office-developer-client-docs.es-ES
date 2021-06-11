---
title: Integración de código de servidor de formulario MAPI Windows código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332182"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integración de código de servidor de formulario MAPI Windows código

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recuerde que el servidor de formularios es una aplicación win32. Por lo tanto, hay algunas tareas relacionadas con cargar el servidor de formularios en la memoria y salir de forma limpia. Al igual que Windows aplicaciones, el punto de entrada del servidor de formularios es la **función WinMain.** Esta función es el lugar adecuado para realizar las siguientes tareas: 
  
- Crear y registrar una clase de ventana para que el servidor de formularios pueda interactuar con otros componentes OLE.
    
- Crear y registrar clases o clases de ventana para las interfaces de usuario de los objetos de formulario.
    
- Llamar a [la función MAPIInitialize.](mapiinitialize.md) **MAPIInitialize también** controla la inicialización OLE necesaria. Esto debe hacerse una vez por instancia del servidor de formulario. 
    
- Registrar un átomo global con una representación de cadena del identificador de clase (CLSID) del servidor de formulario. Este átomo debe existir durante la vigencia del servidor de formulario.
    
- Llamar a la función OLE [CoRegisterClassObject para](https://msdn.microsoft.com/library/ms693407.aspx) registrar la fábrica de clases del servidor de formularios con OLE. 
    
- Crear una ventana principal para recibir mensajes. Es probable que esta ventana no tenga que estar visible porque el usuario interactuará con las ventanas específicas asociadas con objetos de formulario individuales. Sin embargo, durante el desarrollo, la ventana principal puede ser un lugar conveniente para depurar el resultado o el control del servidor de formularios.
    
- Crear un bucle de mensaje que se ejecute durante la vigencia del servidor de formularios, traduciendo y distribuyendo mensajes de Windows a objetos de formulario activos.
    
Al salir del servidor de formularios, debe realizar las siguientes tareas:
  
- Llama a la función OLE [CoRevokeClassObject para](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) revocar el registro OLE de la clase de mensaje. 
    
- Llame **a MAPIUninitialize** para cerrar correctamente la conexión del servidor de formulario a MAPI. 
    
- Elimine el átomo global que contiene la representación de cadena del identificador de clase.
    
## <a name="see-also"></a>Vea también



[Escritura de código de servidor de formulario](writing-form-server-code.md)

