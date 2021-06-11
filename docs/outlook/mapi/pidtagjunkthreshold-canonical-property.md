---
title: Propiedad canónica PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326855"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Propiedad canónica PidTagJunkThreshold

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la agresividad con la que se debe enviar el correo entrante a la carpeta Correo no deseado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Identificador:  <br/> |0x6101  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo no deseado  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad corresponde a la configuración de filtro de alto / bajo / ninguno. Un valor de "0xFFFFFFFF" indica que no se debe aplicar el filtrado de correo no deseado, pero aún deben aplicarse listas de bloqueo. Un valor de "0x80000000" indica que todo el correo es correo no deseado excepto los mensajes de remitentes de la lista de remitentes de confianza o enviados a destinatarios de la lista de destinatarios de confianza. Los valores para esto son los siguientes:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Sin filtrado de correo no deseado  <br/> |
|0x00000006  <br/> |Filtrado de correo no deseado bajo  <br/> |
|0x00000003  <br/> |Filtrado de correo no deseado alto  <br/> |
|0x80000000  <br/> |Solo listas de confianza  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.
    
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

