---
title: Propiedad canónica PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341114"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propiedad canónica PidTagRecipientReassignmentProhibited

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si la adición de destinatarios adicionales, al reenviar el mensaje, está prohibida para el mensaje de correo electrónico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificador:  <br/> |0x002B  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Sobre MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se establece en función del valor del mensaje de correo **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)). Si **PR_SENSITIVITY** se establece en "0x00000000" (normal) o "0x00000003" (confidencial), esta propiedad debe establecerse en "0x00" o ausente, lo que significa que se permite agregar destinatarios adicionales o diferentes al mensaje de correo electrónico. Si el PR_SENSITIVITY  del objeto de correo electrónico está establecido en "0x00000001" (personal) o "0x00000002" (privado), esta propiedad debe establecerse como "0x01" para evitar que se agreguen destinatarios adicionales o diferentes de este correo electrónico mediante el reenvío. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

