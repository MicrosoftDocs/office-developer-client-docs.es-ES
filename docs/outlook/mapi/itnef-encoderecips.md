---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584572"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Codifica una vista de tabla de destinatarios de un mensaje en la secuencia de datos de formato de encapsulación neutro para el transporte (TNEF) para el mensaje.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpRecipientTable_
  
> [entrada] Un puntero a la tabla de destinatarios para el que se codifica la vista. El parámetro _lpRecipientTable_ puede ser NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Transporte proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::EncodeRecips** para llevar a cabo la codificación TNEF para una vista de tabla de destinatarios determinada. La codificación TNEF es útil, por ejemplo, si un proveedor o una puerta de enlace requiere un conjunto de columnas determinado, criterio de ordenación o restricción para la tabla de destinatarios. 
  
Un proveedor o una puerta de enlace pasa la vista de tabla que se desea codificar en el parámetro _lpRecipientTable_ . La implementación de TNEF codifica la tabla de destinatarios con la vista determinada, con el conjunto de columnas determinado, criterio de ordenación, restricción y posición. Si un proveedor o una puerta de enlace pasa NULL en _lpRecipientTable_, TNEF Obtiene la tabla de destinatarios del mensaje se codifica mediante el método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) y procesa cada fila de la tabla en la secuencia de TNEF mediante la configuración actual de la tabla. 
  
Por tanto, al llamar a **EncodeRecips** con NULL _lpRecipientTable_ codifica a todos los destinatarios del mensaje y es equivalente a llamar al método [ITnef::AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE en su parámetro _ulFlags_ y la **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) (propiedad) en su parámetro _lpPropList_ . 
  
Tenga en cuenta que es rara vez es necesario llamar a **EncodeRecips** a menos que haya un requisito para codificar una vista de tabla de destinatarios determinada. Sistemas de mensajería externos casi siempre tengan instalaciones para el tratamiento de las listas de destinatarios que son lo suficientemente eficaces para controlar las necesidades comunes de codificación de las listas de destinatarios; por lo tanto, estos sistemas casi nunca requieran la codificación TNEF para este propósito. 
  
## <a name="see-also"></a>Vea también



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propiedad canónico PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

