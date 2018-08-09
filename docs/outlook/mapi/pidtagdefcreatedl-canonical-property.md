---
title: Propiedad canónica PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819428"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Propiedad canónica PidTagDefCreateDl

  
  
**Hace referencia a**: Outlook 
  
Contiene el identificador de entrada de plantilla para obtener una lista de distribución de forma predeterminada. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Identificador:  <br/> |0x3611  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente usan esta propiedad para crear una lista de distribución dentro de un contenedor. Soporte técnico de la creación de entrada es opcional para los contenedores de la libreta de direcciones; aquellas que no lo admiten no se requieren para exponer esta propiedad. 
  
Esta propiedad especifica una entrada que puede aparecer en la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para las listas de distribución. Después de obtener el identificador, el cliente la utiliza en una llamada al método [IABContainer::CreateEntry](iabcontainer-createentry.md) . La entrada representa la plantilla de la lista de distribución de forma predeterminada. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

