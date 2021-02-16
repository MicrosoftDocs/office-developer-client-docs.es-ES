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
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
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

## <a name="parameters"></a>Parámetros

 _lpvSession_
  
> [entrada] Puntero a la sesión que se va a usar. 
    
 _lpMessage_
  
> [entrada] Puntero al mensaje que se va a preprocesar. 
    
 _lpAdrBook_
  
> [entrada] Puntero a la libreta de direcciones desde la que el usuario debe seleccionar destinatarios para el mensaje. 
    
 _lpFolder_
  
> [entrada, salida] Puntero a una carpeta. En la entrada, el  _parámetro lpFolder_ apunta a la carpeta que contiene los mensajes que se deben preprocesar. En el resultado,  _lpFolder_ apunta a la carpeta donde se han colocado los mensajes preprocesados. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional cuando sea necesario. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
 _lpcOutbound_
  
> [salida] Puntero al número de mensajes de la matriz a los que apunta el _parámetro lpppMessage._ 
    
 _lpppMessage_
  
> [salida] Puntero a un puntero a una matriz de punteros a mensajes preprocesados o generados de otro modo. 
    
 _lppRecipList_
  
> [salida] Puntero a una estructura [ADRLIST](adrlist.md) devuelta opcional, que enumera los destinatarios detectados por el preprocesador para los que el mensaje no se puede entregar. Para obtener más información acerca del contenido de esta lista, vea el método [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El contenido del mensaje se preprocesó correctamente.
    
## <a name="remarks"></a>Comentarios

Un preprocesador de mensajes del proveedor de transporte puede presentar un indicador de progreso durante el preprocesamiento del mensaje. Sin embargo, nunca debe presentar un cuadro de diálogo que requiera la interacción del usuario durante el preprocesamiento del mensaje. 
  
Cuando un preprocesador agrega grandes cantidades de datos a un mensaje saliente, deben seguirse ciertos procedimientos. Este tipo de mensaje se puede almacenar en un almacén de mensajes basado en servidor, lo que hace que el preprocesador tenga acceso a un almacén remoto, un procedimiento que requiere mucho tiempo. Para evitar tener que hacerlo, el preprocesador debe tener una opción que le permita almacenar datos que necesitan una gran cantidad de espacio en un almacén de mensajes local y proporcionar una referencia a ese almacén local en el mensaje. 
  
El preprocesador no debe liberar ninguno de los objetos pasados originalmente a la **función basada en PreprocessMessage.** 
  
Para que la cola MAPI pueda llamar a una función **PreprocessMessage,** el proveedor de transporte debe haber registrado la función en una llamada al método [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) Después de llamar a **una función PreprocessMessage,** la cola no puede continuar enviando un mensaje hasta que la función vuelva. 
  
La cola MAPI es la propietaria de la tarea de enviar mensajes. Esto significa que el mensaje original nunca se coloca en una matriz de punteros de mensaje y que nunca se requiere una llamada a los métodos **SubmitMessage.** 
  
## <a name="see-also"></a>Consulte también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

