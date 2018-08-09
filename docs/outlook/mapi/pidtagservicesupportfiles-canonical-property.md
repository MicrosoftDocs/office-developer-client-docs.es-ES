---
title: Propiedad canónica PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820322"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propiedad canónica PidTagServiceSupportFiles

  
  
**Hace referencia a**: Outlook 
  
Contiene una lista de los archivos que pertenecen al servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificador:  <br/> |0x3D0F  <br/> |
|Tipo de datos:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Uso de un cuadro de diálogo en el applet de panel de control, un usuario puede obtener la lista de archivos que pertenecen al servicio de mensajes. Por ejemplo, el usuario puede obtener los nombres de todas las bibliotecas de vínculos dinámicos (DLL) que pertenecen al servicio. El usuario, a continuación, puede buscar detalles adicionales acerca de los archivos especificados, como los nombres y números de versión de todos los archivos DLL. MAPI utiliza estas propiedades para crear una lista de archivos de soporte técnico en un cuadro de diálogo para la selección del usuario de mensajería.
  
MAPI sólo funciona con los nombres de archivo y otras cadenas pasan a ella, en el juego de caracteres de Interfaces de servicio de Active Directory (ANSI). Las aplicaciones de cliente que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

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

