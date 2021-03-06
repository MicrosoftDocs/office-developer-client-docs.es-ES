---
title: Propiedad canónica PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335423"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>Propiedad canónica PidTagRuleProviderData

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Propiedad opaca que el cliente establece para el uso exclusivo del cliente. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Identificador:  <br/> |0x6684  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

El servidor debe conservar el valor de esta propiedad si lo estableció el cliente, pero debe omitir su contenido durante la evaluación y el procesamiento de reglas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrantes en un servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas. 
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

