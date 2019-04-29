---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437248"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función que preprocesa el contenido del mensaje o el formato de un mensaje.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi. h  <br/> |
|Función definida implementada por:  <br/> |Proveedores de transporte  <br/> |
|Función definida llamada por:  <br/> |Cola MAPI  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>Parameters

 _lpvSession_
  
> a Puntero a la sesión que se va a usar. 
    
 _lpMessage_
  
> a Puntero al mensaje que se preprocesará. 
    
 _lpAdrBook_
  
> a Puntero a la libreta de direcciones de la que el usuario debe seleccionar los destinatarios del mensaje. 
    
 _lpFolder_
  
> [in, out] Puntero a una carpeta. En la entrada, el parámetro _lpFolder_ apunta a la carpeta que contiene los mensajes que se preprocesarán. En la salida, _lpFolder_ apunta a la carpeta donde se han colocado los mensajes preprocesados. 
    
 _lpAllocateBuffer_
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
 _lpAllocateMore_
  
> a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional donde sea necesario. 
    
 _lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpcOutbound_
  
> contempla Puntero al número de mensajes de la matriz señalado por el parámetro _lpppMessage_ . 
    
 _lpppMessage_
  
> contempla Puntero a un puntero a una matriz de punteros a mensajes preprocesados o generados de otra manera. 
    
 _lppRecipList_
  
> contempla Puntero a una estructura [ADRLIST](adrlist.md) devuelta opcional, que enumera los destinatarios detectados como preprocesadores para los que el mensaje no se entregó. Para obtener más información sobre el contenido de esta lista, vea el método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El contenido del mensaje se ha preprocesado correctamente.
    
## <a name="remarks"></a>Comentarios

Un preprocesador de mensajes de proveedor de transporte puede presentar un indicador de progreso durante el preprocesamiento de mensajes. Sin embargo, nunca debe presentar un cuadro de diálogo que requiera la interacción del usuario durante el preprocesamiento de mensajes. 
  
Cuando un preprocesador agrega grandes cantidades de datos a un mensaje saliente, se deben seguir ciertos procedimientos. Este tipo de mensaje puede almacenarse en un almacén de mensajes basado en servidor, lo que hace que el preprocesador obtenga acceso a un almacén remoto, un procedimiento que requiere mucho tiempo. Para evitar tener que hacerlo, el preprocesador debe tener una opción que permite almacenar datos que ocupan una gran cantidad de espacio en un almacén de mensajes local y proporcionar una referencia al almacén local en el mensaje. 
  
El preprocesador no debe liberar ninguno de los objetos pasados originalmente a la función basada en **PreprocessMessage** . 
  
Antes de que la cola MAPI pueda llamar a una función **PreprocessMessage** , el proveedor de transporte debe haber registrado la función en una llamada al método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Después de llamar a una función **PreprocessMessage** , la cola de impresión no puede seguir enviando un mensaje hasta que la función devuelve. 
  
La cola MAPI posee la tarea de enviar mensajes. Esto significa que el mensaje original nunca se coloca en una matriz de punteros de mensaje y que una llamada a los métodos **SubmitMessage** nunca es necesaria. 
  
## <a name="see-also"></a>Ver también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

