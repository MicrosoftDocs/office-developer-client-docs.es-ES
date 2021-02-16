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
  
Completa la lista de destinatarios de un mensaje, expandiendo listas de distribución concretas.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Puntero al mensaje que tiene que procesarse la lista de destinatarios.
    
 _lpulFlags_
  
> [salida] Puntero a una máscara de bits de marcas que controla el tipo de procesamiento que se produce. Se pueden establecer las siguientes marcas:
    
NEEDS_PREPROCESSING 
  
> El mensaje debe preprocesarse antes de que se envíe.
    
NEEDS_SPOOLER 
  
> La cola MAPI (en lugar del proveedor de transporte al que está estrechamente unido el autor de la llamada) debe enviar el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios del mensaje se procesó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::ExpandRecips** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes. Los proveedores de almacén de mensajes **llaman a ExpandRecips** para solicitar a MAPI que realice las siguientes tareas: 
  
- Expanda determinadas listas de distribución personales a los destinatarios de sus componentes.
    
- Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.
    
- Marca las entradas duplicadas.
    
- Resolver todas las direcciones de un solo servidor. 
    
- Compruebe si el mensaje necesita preprocesamiento y, si es así, establezca la marca a la que  _apunta lpulFlags_ en NEEDS_PREPROCESSING. 
    
 **ExpandRecips expande** las listas de distribución que tienen el tipo de dirección de mensajería MAPIPDL. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame siempre **a ExpandRecips** como parte del procesamiento de mensajes. Realiza una llamada a **ExpandRecips una** de las primeras llamadas en la implementación del método [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="see-also"></a>Consulte también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

