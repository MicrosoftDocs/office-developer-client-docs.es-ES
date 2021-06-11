---
title: Propiedad canónica PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339336"
---
# <a name="pidtagattachflags-canonical-property"></a>Propiedad canónica PidTagAttachFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas para un dato adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Identificador:  <br/> |0x3714  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para la compatibilidad con MHTML. 
  
Se pueden establecer una o varias de las siguientes marcas **para la máscara PR_ATTACH_FLAGS** bits: 
  
ATT_INVISIBLE_IN_HTML 
  
> Indica que estos datos adjuntos no están disponibles para las aplicaciones de representación HTML y deben omitirse en el procesamiento de extensiones multipropósito de correo de Internet (MIME). 
    
ATT_INVISIBLE_IN_RTF 
  
> Indica que estos datos adjuntos no están disponibles para la representación de aplicaciones en formato de texto enriquecido (RTF) y mapi debe omitirlos.
    
Si la **PR_ATTACH_FLAGS** es cero o ausente, todas las aplicaciones procesarán los datos adjuntos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

