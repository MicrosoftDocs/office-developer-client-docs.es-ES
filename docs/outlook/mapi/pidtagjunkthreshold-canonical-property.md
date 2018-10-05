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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387114"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Propiedad canónica PidTagJunkThreshold

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Agresividad indica el correo entrante se debe enviar a la carpeta correo electrónico no deseado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Identificador:  <br/> |0x6101  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad corresponde a la alta / baja / ninguna configuración de filtro. Un valor de "0xFFFFFFFF" indica que el filtrado de spam no se debe aplicar, sin embargo, aún se deben aplicar las listas de bloqueados. Un valor de "0 x 80000000" indica que todo el correo se spam, excepto los mensajes de remitentes de la lista de remitentes de confianza o se envía a los destinatarios de la lista de destinatarios de confianza. Los valores de esto son los siguientes:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Sin filtrado de spam  <br/> |
|0 x 00000006  <br/> |Filtrado de spam baja  <br/> |
|0 x 00000003  <br/> |Filtrado de spam alta  <br/> |
|0 x 80000000  <br/> |Sólo listas de confianza  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.
    
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

