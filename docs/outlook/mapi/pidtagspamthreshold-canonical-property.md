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
ms.openlocfilehash: d43a0229f232f9437d1746799534c0f2d6fba83f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346315"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propiedad canónica PidTagSpamThreshold

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valor de tipo Long que indica el nivel de filtrado de correo no deseado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|IDENTIFICADOR largo (LID):  <br/> | 0x041B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo no deseado  <br/> |
   
## <a name="values"></a>Valores

Los valores para el filtrado de correo no deseado son los siguientes:
  
|**Nivel de correo no deseado**|**Value**|
|:-----|:-----|
|Ninguno  <br/> |0xFFFFFFFF  <br/> |
|Bajo  <br/> |0x00000006  <br/> |
|Medio  <br/> |0x00000005  <br/> |
|Alta  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.
    
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

