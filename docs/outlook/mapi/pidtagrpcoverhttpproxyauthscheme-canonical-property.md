---
title: Propiedad canónica PidTagRpcOverHttpProxyAuthScheme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8c68c2cd34ba037dc725a7d15575159466d8123
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820118"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>Propiedad canónica PidTagRpcOverHttpProxyAuthScheme

  
  
**Hace referencia a**: Outlook 
  
Representa el protocolo de autenticación que se usará para este perfil.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|Identificador:  <br/> |0x6627  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se puede establecer para la autenticación básica o autenticación de NT LAN Manager (NTLM). Los valores posibles para esta propiedad son los siguientes.
  
|**Nombre**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0 x 1  <br/> |Autenticación básica  <br/> |
|**ROHAUTH_NTLM** <br/> |0 x 2  <br/> |Autenticación NTLM  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicos que se usan en las operaciones remotas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
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

