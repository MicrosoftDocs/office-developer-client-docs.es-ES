---
title: Llamar a MAPI desde servicios de Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385581"
---
# <a name="calling-mapi-from-windows-services"></a>Llamar a MAPI desde servicios de Windows

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para habilitar las aplicaciones de cliente MAPI que se escriben como servicios de Windows para que funcione con los proveedores de servicio compatible con MAPI, MAPI impone varias limitaciones y requisitos.
  
Los clientes MAPI tienen las siguientes limitaciones:
  
- No se permiten una interfaz de usuario.
    
- Pueden enviar mensajes a través de un almacén de mensajes acoplado y transporte de proveedor. Además, los clientes MAPI pueden enviar y recibir mensajes utilizando sólo el servidor de Exchange de Microsoft u otro proveedor de transporte basadas en servidor. Debido a problemas de identidad y la seguridad entre las aplicaciones de cliente y la cola MAPI, la mayoría de los proveedores de transporte no se admite en un servicio. 
    
Todas las aplicaciones de cliente MAPI, si se implementan como servicios de Windows, deben llamar a la función [MAPIInitialize](mapiinitialize.md) para inicializar las bibliotecas de MAPI. Una llamada a la función [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) también es necesaria usar las bibliotecas de OLE. [MAPIInitialize](mapiinitialize.md) y [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) realizan llamadas a la función [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) para inicializar las bibliotecas de modelo de objetos componentes (COM). Los clientes que son servicios deben establecer un indicador especial, MAPI_NT_SERVICE, en el miembro **ulFlags** de la estructura [MAPIINIT_0](mapiinit_0.md) que se pasa a [MAPIInitialize](mapiinitialize.md) y en el parámetro _ulFlags_ que se pasa a la [MAPILogonEx](mapilogonex.md) función para informar a MAPI de su implementación especial. 
  
Los clientes MAPI que se escriben como servicios de Windows y se escribe con la interfaz de cliente MAPI tienen un requisito adicional. Debe establecer la marca MAPI_NO_MAIL en la llamada a [MAPILogonEx](mapilogonex.md). Otros tipos de clientes no es necesario que establecer una marca de inicio de sesión debido a que se establece automáticamente por MAPI.
  
Para administrar los mensajes en un subproceso de inicialización, un cliente MAPI que se implementa como un servicio hace lo siguiente:
  
1. Llama a la función [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) cuando el subproceso principal se bloquea. 
    
2. Llama a la secuencia [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)y [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) de funciones de Windows para administrar el mensaje cuando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) devuelve la suma del valor del parámetro _nCount_ y el valor de **WAIT_OBJECT_0**, que indica que es un mensaje en la cola.
    
## <a name="see-also"></a>Vea también



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas del entorno operativo](operating-environment-issues.md)

