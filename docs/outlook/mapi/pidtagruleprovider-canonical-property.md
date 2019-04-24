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
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280608"
---
# <a name="pidtagruleprovider-canonical-property"></a>Propiedad canónica PidTagRuleProvider

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de la aplicación que establece una regla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Identificador:  <br/> |0x6681  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Las acciones diferidas necesitan estas propiedades para identificar el código que debe interpretar y ejecutar la acción de regla.
  
Las reglas almacenadas en buzones y carpetas se asocian con la aplicación que las posee mediante una cadena de proveedor de reglas. Un proveedor de reglas establece y controla las reglas de una tabla de reglas. También proporciona un medio para controlar las acciones diferidas si estas reglas se establecen. El almacén de información crea implícitamente las acciones diferidas. Para las operaciones de movimiento o copia en un almacén diferente, si un proveedor establece una regla de acción diferida, debe proporcionar un controlador para realizar la acción cuando se activa la regla y se crea una acción diferida.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrantes en un servidor.
    
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

