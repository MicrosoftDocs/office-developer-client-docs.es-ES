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
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417045"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propiedad canónica PidTagServiceSupportFiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de los archivos que pertenecen al servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificador:  <br/> |0x3D0F  <br/> |
|Tipo de datos:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Mediante un cuadro de diálogo en el applet del panel de control, un usuario puede obtener la lista de archivos que pertenecen al servicio de mensajes. Por ejemplo, el usuario puede obtener los nombres de todas las bibliotecas de vínculos dinámicos (DLL) que pertenecen al servicio. A continuación, el usuario puede buscar detalles adicionales sobre los archivos especificados, como los nombres y números de versión de todas las DLL. MAPI usa estas propiedades para crear una lista de archivos de compatibilidad en un cuadro de diálogo para la selección del usuario de mensajería.
  
MAPI sólo funciona con nombres de archivo y otras cadenas pasadas en el juego de caracteres de interfaces de servicio de Active Directory (ANSI). Las aplicaciones cliente que usan nombres de archivo en un juego de caracteres oem (fabricante de equipos originales) deben convertirlos en ANSI antes de llamar a MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

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

