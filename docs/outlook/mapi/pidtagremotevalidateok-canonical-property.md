---
title: Propiedad canónica PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9b06ebbe8cb162d77d60cfffa866438567c84c27
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576837"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propiedad canónica PidTagRemoteValidateOk

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene TRUE si se permite el visor remoto para llamar al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificador:  <br/> |0x3E0D  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad aparece en la tabla de estado y ofrece cierto control sobre el rendimiento de transporte. Se puede considerar como otra manera de dirigir al visor remoto a inactivo. Cuando se establece en TRUE, el visor remoto puede llamar a **IMAPIStatus::ValidateState** tantas veces como desee. Un valor de FALSE indica que el visor remoto no puede realizar ninguna llamada. 
  
El proveedor de transporte normalmente establece esta propiedad dinámicamente, con estableciendo el valor en FALSE para deshabilitar las llamadas adicionales cuando el proveedor de transporte tiene una cantidad suficiente de procesamiento para llevar a cabo. Cuando se realiza el proveedor de transporte, a continuación, Establece el valor en TRUE para permitir que la aplicación cliente realizar más llamadas de **IMAPIStatus::ValidateState** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

