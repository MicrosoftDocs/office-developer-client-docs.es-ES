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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316530"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Completa la lista de destinatarios de un mensaje y expande listas de distribución particulares.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> a Un puntero al mensaje que tiene la lista de destinatarios que se procesará.
    
 _lpulFlags_
  
> contempla Puntero a una máscara de máscara de marcadores que controla el tipo de procesamiento que se produce. Se pueden establecer los siguientes indicadores:
    
NEEDS_PREPROCESSING 
  
> Es necesario preprocesar el mensaje antes de enviarlo.
    
NEEDS_SPOOLER 
  
> La cola MAPI (en lugar del proveedor de transporte al que la persona que llama está estrechamente acoplada) debe enviar el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios del mensaje se ha procesado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: ExpandRecips** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes llaman a **ExpandRecips** para pedir a MAPI que realice las siguientes tareas: 
  
- ExPanda algunas listas de distribución personales a sus destinatarios del componente.
    
- Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.
    
- Marque las entradas duplicadas.
    
- Resuelva todas las direcciones de un solo uso. 
    
- Compruebe si el mensaje necesita preprocesamiento y, si es así, establezca la marca apuntada por _lpulFlags_ a NEEDS_PREPROCESSING. 
    
 **ExpandRecips** expande las listas de distribución que tienen el tipo de dirección de mensajería de MAPIPDL. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame siempre a **ExpandRecips** como parte del procesamiento de mensajes. Realice una llamada a **ExpandRecips** una de las primeras llamadas en la implementación del método [IMessage:: SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

