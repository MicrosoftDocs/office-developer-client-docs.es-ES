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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315389"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propiedad canónica PidLidValidFlagStringProof

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida si el valor de la propiedad **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) lo estableció un agente que conocía el valor de la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidValidFlagStringProof  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x000085BF  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

En objetos no enviados (correo recibido y objetos que no son de correo), los clientes deben establecer este valor en el valor de **PR_MESSAGE_DELIVERY_TIME** al modificar **dispidRequest**.
  
Dado que el remitente no puede predecir el valor de **PR_MESSAGE_DELIVERY_TIME,** si el valor de esta propiedad es igual al valor de **PR_MESSAGE_DELIVERY_TIME**, es razonablemente seguro que el valor de **dispidRequest** no se originó en el remitente del mensaje. Un cliente puede decidir cómo presentar el valor de **dispidRequest** al usuario final en función del resultado de esta comparación de acuerdo con la directiva de seguridad específica del cliente. Si se omite el valor **de dispidRequest** debido a la presencia de un valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), esta propiedad debe omitirse.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

