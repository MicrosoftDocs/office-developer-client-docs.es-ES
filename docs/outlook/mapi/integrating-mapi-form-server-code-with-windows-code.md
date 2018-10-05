---
title: Integración de código de servidor de formulario MAPI con código de Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397866"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integración de código de servidor de formulario MAPI con código de Windows

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Recuerde que el servidor de formulario es una aplicación de Win32. Por lo tanto, hay algunas tareas relacionadas con la carga de su servidor de formulario en la memoria y salir sin problemas. Al igual que todas las aplicaciones de Windows, el punto de entrada para el servidor de formulario es la función **WinMain** . Esta función es el lugar adecuado para realizar las siguientes tareas: 
  
- Crear y registrar una clase de ventana para que su servidor de formulario puede interactuar con otros componentes OLE.
    
- Crear y registrar una clase de ventana o las clases para las interfaces de usuario de los objetos del formulario.
    
- Llamar a la función de [MAPIInitialize](mapiinitialize.md) . **MAPIInitialize** administra la OLE inicialización necesaria para usted, así como. Debe realizarse una vez por cada instancia de su servidor del formulario. 
    
- Registrar un atom global con una representación de cadena del identificador de clase (CLSID) del servidor de formulario. Este atom debería haber por la duración del servidor de formulario.
    
- Llamar a la función OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar el generador de clases del servidor de su formulario con OLE. 
    
- Creación de una ventana principal para recibir los mensajes. Probablemente esta ventana no necesita ser visible, ya que el usuario interactúa con la versión de windows asociados con los objetos de formulario individuales. Sin embargo, durante el desarrollo, la ventana principal de puede ser un lugar adecuado para la depuración de salida o el control de su servidor del formulario.
    
- Creación de un bucle de mensajes que se ejecuta para la duración del servidor de formulario, traducir y enviar mensajes de windows a los objetos del formulario activo.
    
Cuando sale de su servidor de formulario, debe realizar las siguientes tareas:
  
- Llame a la función OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revocar el registro OLE de la clase de mensaje. 
    
- Llamar a **MAPIUninitialize** para cerrar correctamente la conexión del servidor de formulario a MAPI. 
    
- Eliminar el atom global que contiene la representación de cadena del identificador de clase.
    
## <a name="see-also"></a>Vea también



[Escribir código de servidor de formulario](writing-form-server-code.md)

