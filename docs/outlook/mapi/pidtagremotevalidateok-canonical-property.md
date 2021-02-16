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
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424227"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propiedad canónica PidTagRemoteValidateOk

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene TRUE si el visor remoto puede llamar al [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificador:  <br/> |0x3E0D  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad aparece en la tabla de estado y ofrece cierto control sobre el rendimiento del transporte. Se puede considerar como otra forma de dirigir el visor remoto a inactivo. Cuando se establece en TRUE, el visor remoto puede llamar a **IMAPIStatus::ValidateState** tantas veces como desee. Un valor FALSE indica que el visor remoto no puede realizar más llamadas. 
  
Normalmente, el proveedor de transporte establece esta propiedad dinámicamente, estableciendo el valor en FALSE para deshabilitar llamadas adicionales cuando el proveedor de transporte tiene una cantidad suficiente de procesamiento para realizar. Una vez terminado el proveedor de transporte, establece el valor en TRUE para permitir que la aplicación cliente realice más llamadas **IMAPIStatus::ValidateState.** 
  
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

