---
title: Propiedad canónica PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7c5cfa8f80895896eab9af5ce1f249b9b06cf425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819862"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>Propiedad canónica PidTagOriginatingMtaCertificate

  
  
**Hace referencia a**: Outlook 
  
Contiene un identificador para el agente de transferencia de mensajes (MTA) que se originó el mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x0E25  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad, si se establece, está disponible en envía los mensajes en la carpeta Elementos enviados.
  
Esta propiedad corresponde al atributo X.400 informe por mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

