---
title: Propiedad canónica PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420643"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propiedad canónica PidTagRecipientNumberForAdvice

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene el número de teléfono de un destinatario del mensaje al que llamar para informar de la entrega física de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Identificador:  <br/> |0x0C14  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades están diseñadas para usarse junto con la entrega a un destino físico, en lugar de un buzón electrónico, cuando no se espera que el destinatario humano esté presente en la entrega. Un ejemplo es el número de teléfono de una hoja de portada de fax.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

