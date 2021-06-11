---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411249"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Completa la lista de destinatarios de un mensaje, expandiendo listas de distribución determinadas.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Puntero al mensaje que tiene la lista de destinatarios que se va a procesar.
    
 _lpulFlags_
  
> [salida] Puntero a una máscara de bits de marcas que controla el tipo de procesamiento que se produce. Se pueden establecer las siguientes marcas:
    
NEEDS_PREPROCESSING 
  
> El mensaje debe procesarse previamente antes de que se envíe.
    
NEEDS_SPOOLER 
  
> La cola MAPI (en lugar del proveedor de transporte al que el autor de la llamada está estrechamente acoplado) debe enviar el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios del mensaje se procesó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::ExpandRecips** se implementa para objetos de soporte del proveedor del almacén de mensajes. Los proveedores de almacén de mensajes **llaman a ExpandRecips** para solicitar a MAPI que realice las siguientes tareas: 
  
- Expande determinadas listas de distribución personales a sus destinatarios de componentes.
    
- Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.
    
- Marca las entradas duplicadas.
    
- Resuelva todas las direcciones únicas. 
    
- Compruebe si el mensaje necesita preprocesamiento y, si lo hace, establezca la marca que  _apunta lpulFlags_ en NEEDS_PREPROCESSING. 
    
 **ExpandRecips** expande cualquier lista de distribución que tenga el tipo de dirección de mensajería mapipdl. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llama siempre **a ExpandRecips** como parte del procesamiento de mensajes. Realice una llamada a **ExpandRecips una** de las primeras llamadas en la implementación del método [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

