---
title: Propiedad canónica PidTagOriginatorCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d367073de2134ff766cbae3d4f6bcfa30b862122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351110"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a>Propiedad canónica PidTagOriginatorCertificate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un certificado ASN. 1 para el autor del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINATOR_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x0022  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una copia de la propiedad **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) del autor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

