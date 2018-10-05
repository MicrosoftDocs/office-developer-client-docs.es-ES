---
title: Propiedad canónica PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384972"
---
# <a name="pidtagbodyhtml-canonical-property"></a>Propiedad canónica PidTagBodyHtml

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la versión de lenguaje de marcado de hipertexto (HTML) del texto del mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W  <br/> |
|Identificador:  <br/> |0x1013  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades contienen el mismo texto del mensaje como **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), pero en HTML. 
  
Un almacén de mensajes que admite HTML indica que esta estableciendo el indicador **STORE_HTML_OK** en su **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
 **Nota** **STORE_HTML_OK** no está definido en las versiones de Mapidefs.h que se incluye con Microsoft® Exchange 2000 Server y versiones anteriores. Si **STORE_HTML_OK** no está definido, use el valor 0 x 00010000 en su lugar. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

