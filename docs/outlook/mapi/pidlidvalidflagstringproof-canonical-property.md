---
title: Propiedad canónica PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391958"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propiedad canónica PidLidValidFlagStringProof

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Valida si el valor de la propiedad **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) se estableció por un agente que conoce el valor de la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidValidFlagStringProof  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x000085BF  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

En los objetos que no se puedan enviar (correo recibido y objetos que no sean de correo), los clientes deben establecer este valor en el valor de **PR_MESSAGE_DELIVERY_TIME** al modificar **dispidRequest**.
  
Dado que no se puede predecir el valor de **PR_MESSAGE_DELIVERY_TIME** por el remitente, si el valor de esta propiedad es igual al valor de **PR_MESSAGE_DELIVERY_TIME**, es razonablemente seguro de que el valor de **dispidRequest** no lo hizo se originan desde el remitente del mensaje. Un cliente puede decidir cómo presentar el valor de **dispidRequest** para el usuario final en función del resultado de esta comparación con arreglo a la directiva de seguridad específicos del cliente. Si se omite el valor de **dispidRequest** debido a la presencia de un valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), debe ignorarse esta propiedad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

