---
title: Llamar a MAPI desde Windows Services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318111"
---
# <a name="calling-mapi-from-windows-services"></a>Llamar a MAPI desde Windows Services

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para permitir que las aplicaciones cliente MAPI que se escriben como servicios Windows funcionen con proveedores de servicios compatibles con MAPI, MAPI impone varias limitaciones y requisitos.
  
Los clientes MAPI tienen las siguientes limitaciones:
  
- No pueden permitir una interfaz de usuario.
    
- Solo pueden enviar mensajes a través de un proveedor de transporte y un almacén de mensajes estrechamente acoplados. Además, los clientes MAPI pueden enviar y recibir mensajes mediante el Microsoft Exchange Server u otro proveedor de transporte basado en servidor. Debido a problemas de identidad y seguridad entre las aplicaciones cliente y la cola MAPI, la mayoría de los proveedores de transporte no se admiten en un servicio. 
    
Todas las aplicaciones cliente MAPI, tanto si se implementan como servicios Windows, deben llamar a la [función MAPIInitialize](mapiinitialize.md) para inicializar las bibliotecas MAPI. También es necesaria una llamada [a la función OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para usar las bibliotecas OLE. Tanto [MAPIInitialize](mapiinitialize.md) como [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) hacen llamadas a la función [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) para inicializar las bibliotecas del Modelo de objetos componentes (COM). Los clientes que son servicios deben establecer una marca especial, MAPI_NT_SERVICE, en el **miembro ulFlags** de la estructura [de MAPIINIT_0](mapiinit_0.md) que se pasa a [MAPIInitialize](mapiinitialize.md) y en el parámetro  _ulFlags_ que se pasa a la función [MAPILogonEx](mapilogonex.md) para informar a MAPI de su implementación especial. 
  
Los clientes MAPI escritos como Windows y escritos con la interfaz de cliente MAPI tienen un requisito adicional. Deben establecer la marca MAPI_NO_MAIL en la llamada en [MAPILogonEx](mapilogonex.md). Otros tipos de clientes no tienen que establecer una marca para el inicio de sesión porque MAPI la establece automáticamente.
  
Para controlar los mensajes en un subproceso de inicialización, un cliente MAPI que se implementa como servicio hace lo siguiente:
  
1. Llama a [la función MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) cuando el subproceso principal se bloquea. 
    
2. Llama a la secuencia [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)y [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) de las funciones Windows para controlar el mensaje cuando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) devuelve la suma del valor del parámetro _nCount_ y el valor de **WAIT_OBJECT_0**, lo que indica que un mensaje está en la cola.
    
## <a name="see-also"></a>Vea también



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas del entorno operativo](operating-environment-issues.md)

