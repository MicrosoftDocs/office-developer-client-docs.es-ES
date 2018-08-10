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
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820441"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Hace referencia a**: Outlook 
  
Define una función que preprocesa el contenido del mensaje o el formato de un mensaje.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Función definido implementada por:  <br/> |Proveedores de transporte  <br/> |
|Llamado por una función definida:  <br/> |Cola MAPI  <br/> |
   
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
  
> [entrada] Puntero a la sesión que se va a utilizar. 
    
 _lpMessage_
  
> [entrada] Puntero al mensaje para que se preprocesan. 
    
 _lpAdrBook_
  
> [entrada] Puntero a la libreta de direcciones desde el que el usuario debe seleccionar los destinatarios del mensaje. 
    
 _lpFolder_
  
> [entrada, salida] Puntero a una carpeta. En la entrada, el parámetro _lpFolder_ apunta a la carpeta que contiene los mensajes que se preprocesan. En la salida, _lpFolder_ apunta a la carpeta donde se han establecido los mensajes preprocesados. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional cuando sea necesario. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpcOutbound_
  
> [out] Puntero al número de mensajes en la matriz indicada por el parámetro _lpppMessage_ . 
    
 _lpppMessage_
  
> [out] Puntero a un puntero a una matriz de punteros a preprocesa o en caso contrario, los mensajes generados. 
    
 _lppRecipList_
  
> [out] Puntero a una estructura [ADRLIST](adrlist.md) devuelta opcional, listado a detecta preprocesador de destinatarios para los que es no se puede entregar el mensaje. Para obtener más información sobre el contenido de esta lista, vea el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El contenido del mensaje se han preprocesado correctamente.
    
## <a name="remarks"></a>Comentarios

Un preprocesador de mensaje del proveedor de transporte puede presentar un indicador de progreso durante el preprocesamiento del mensaje. Sin embargo, nunca debe presentar un cuadro de diálogo requerir la interacción del usuario durante el preprocesamiento del mensaje. 
  
Cuando un preprocesador agrega grandes cantidades de datos a un mensaje saliente, deben seguir ciertos procedimientos. Este tipo de mensaje puede almacenarse en un almacén de mensajes basado en servidor, lo que provoca que el preprocesador tener acceso a un almacén remoto, un procedimiento mucho tiempo. Para evitar tener que volver a hacerlo, el preprocesador debe tener una opción que le permite almacenar los datos que toma una gran cantidad de espacio en un almacén de mensajes local y para proporcionar una referencia a dicho almacén local en el mensaje. 
  
El preprocesador no debe liberar cualquiera de los objetos que originalmente se pasan a la función **PreprocessMessage** en función. 
  
Antes de la cola MAPI puede llamar a una función **PreprocessMessage** , el proveedor de transporte debe tener registrados la función en una llamada al método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Después de llamar a una función **PreprocessMessage** , la cola de impresión no puede continuar el envío de un mensaje hasta que devuelve la función. 
  
La cola MAPI propietario de la tarea de envío de mensajes. Esto significa que el mensaje original nunca se coloca en una matriz de punteros de mensaje y que nunca se requiere una llamada a los métodos de **SubmitMessage** . 
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

