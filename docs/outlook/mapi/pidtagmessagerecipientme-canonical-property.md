---
title: Propiedad canónica PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325623"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propiedad canónica PidTagMessageRecipientMe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si este usuario de mensajería se denomina específicamente como destinatario principal (Para), copia de carbono (CC) o copia de carbón ciego (CCO) destinatario de este mensaje y no forma parte de una lista de distribución. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificador:  <br/> |0x0059  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona una forma cómoda de determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios, sin examinar todas las entradas de la lista. El valor representa la operación **OR** lógica de las propiedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) y **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) y la información CCO (que de lo contrario no aparece en una propiedad). 
  
Esta propiedad ayuda al tratamiento automatizado de los mensajes recibidos en el momento de la recepción. En la opción del proveedor de transporte, esta propiedad contiene FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios. 
  
La entrega de mensajes que resulta de la expansión de la lista de distribución no hace que se establezca esta propiedad. El destinatario debe tener un nombre explícito. 
  
Por lo general, los mensajes no enviados no establecen esta propiedad, **PR_MESSAGE_CC_ME**, o **PR_MESSAGE_TO_ME**. Si están presentes en mensajes a los que el usuario puede acceder en almacenes de mensajes públicos, en almacenes privados de otros usuarios, en archivos en disco o incrustados dentro de otros mensajes recibidos, generalmente contienen los valores a los que se les estableció la última vez que un proveedor de transporte entregó el mensaje. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.
    
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

