---
title: Propiedad canónica PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278876"
---
# <a name="pidtagmailpermission-canonical-property"></a>Propiedad canónica PidTagMailPermission

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el usuario de mensajería puede enviar y recibir mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MAIL_PERMISSION  <br/> |
|Identificador:  <br/> |0x3A0E  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Si no se establece esta propiedad, MAPI la trata como si tuviera un valor TRUE. 
  
Establezca esta propiedad en FALSE en un directorio corporativo donde algunas de las entradas no están habilitadas para correo electrónico. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

