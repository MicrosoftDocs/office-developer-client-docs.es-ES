---
title: Propiedad canónica PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342507"
---
# <a name="pidtagsensitivity-canonical-property"></a>Propiedad canónica PidTagSensitivity

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica la opinión del remitente del mensaje sobre la sensibilidad de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SENSITIVITY  <br/> |
|Identificador:  <br/> |0x0036  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los objetos de mensaje exponán esta propiedad.
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
SENSITIVITY_NONE 
  
> El mensaje no tiene confidencialidad especial.
    
SENSITIVITY_PERSONAL 
  
> El mensaje es personal.
    
SENSITIVITY_PRIVATE 
  
> El mensaje es privado.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> El mensaje se designa como confidencial de la empresa.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

