---
title: Propiedad canónica PidTagSpamThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9a5e72a585a2af8914b858cb4d174899706797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566778"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propiedad canónica PidTagSpamThreshold

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un valor de tipo long que indica el nivel de filtrado de spam.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Identificador de tipo Long (LID):  <br/> | 0x041B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Values

Los valores de filtrado de spam son los siguientes:
  
|**Nivel de correo no deseado**|**Valor**|
|:-----|:-----|
|Ninguna  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Medio  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

