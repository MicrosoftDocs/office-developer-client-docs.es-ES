---
title: Propiedad canónica PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5456e0abffd1ac25983809d32fde88644eaa01cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820176"
---
# <a name="pidtagruleprovider-canonical-property"></a>Propiedad canónica PidTagRuleProvider

  
  
**Hace referencia a**: Outlook 
  
Contiene el nombre de la aplicación que establece una regla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Identificador:  <br/> |0x6681  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Reglas del servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Aplaza necesidad de acciones estas propiedades para identificar el código que se deben interpretar y ejecutar la acción de regla.
  
Las reglas almacenadas en los buzones de correo y las carpetas están asociadas con la aplicación que es el propietario por una cadena de proveedor de la regla. Un proveedor de regla establece y administra las reglas en una tabla de reglas. También proporciona un medio de controlar todas las acciones diferidas si estas reglas están establecidas. Acciones diferidas se crean implícitamente por el almacén de información. Para las operaciones de mover o copiar a un almacén diferente, si un proveedor establece una regla de acción aplazada, debe proporcionar un controlador para llevar a cabo la acción cuando se desencadena la regla y se crea una acción aplazada.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrante en un servidor.
    
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

