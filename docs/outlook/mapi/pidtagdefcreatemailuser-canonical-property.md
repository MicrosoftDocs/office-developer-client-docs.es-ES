---
title: Propiedad canónica PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407483"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Propiedad canónica PidTagDefCreateMailuser

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de plantilla para un objeto de usuario de mensajería predeterminado. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Identificador:  <br/> |0x3612  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente usan esta propiedad para crear un objeto de usuario de mensajería dentro de un contenedor. La compatibilidad con la creación de entradas es opcional para los contenedores de la libreta de direcciones; los usuarios que no la admitan no necesitan exponer esta propiedad. 
  
Esta propiedad especifica una entrada que puede aparecer en la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para los usuarios de mensajería. Después de obtener el identificador, el cliente lo usa en una llamada al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) . La entrada representa la plantilla para el usuario de correo predeterminado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

