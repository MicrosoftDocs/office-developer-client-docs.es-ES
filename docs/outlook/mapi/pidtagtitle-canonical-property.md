---
title: Propiedad canónica PidTagTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388283"
---
# <a name="pidtagtitle-canonical-property"></a>Propiedad canónica PidTagTitle

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el título del trabajo del destinatario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TITLE, PR_TITLE_A, PR_TITLE_W  <br/> |
|Identificador:  <br/> |0x3A17  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Usuario de correo MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades proporcionan identificación y obtener acceso a información de un destinatario. Se definen por el destinatario y la organización del destinatario. 
  
Estas propiedades se usan con frecuencia para indicar el título del destinatario trabajo formal, como programador, en lugar de clase profesional, como programador. No se usa normalmente para los títulos de un "sufijo" como Esq. o DDS.
  
Valores comunes para esta propiedad se incluyen: Director general, programador II, profesor asociado y responsable de desarrollo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
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

