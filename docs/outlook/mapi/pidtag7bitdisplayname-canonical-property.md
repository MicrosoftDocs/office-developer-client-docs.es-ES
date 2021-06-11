---
title: Propiedad canónica PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315816"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a>Propiedad canónica PidTag7BitDisplayName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una representación ASCII de 7 bits del nombre de un usuario de mensajería. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x39FF  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades asignan **la PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en un juego de caracteres de 7 bits. Algunos sistemas de mensajería, como Internet y determinados vínculos X.400, están limitados al conjunto de código ASCII de 128 caracteres de 7 bits. Las puertas de enlace a estos sistemas de mensajería pueden mejorar su rendimiento llamando al método [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) directamente para recuperar la propiedad, lo que evita el procesamiento adicional para la conversión de código. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones en listas de usuarios, contactos, grupos y recursos.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Controla las comunicaciones de un cliente con un servidor NSPI.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de datos que se usa para transferencias de datos entre el cliente y el servidor.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

