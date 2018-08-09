---
title: Propiedad canónica PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820120"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propiedad canónica PidTagRpcOverHttpFlags

  
  
**Hace referencia a**: Outlook 
  
Contiene la configuración en un perfil utilizado por Microsoft Office Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROH_FLAGS  <br/> |
|Identificador:  <br/> |0x6623  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad **PR_ROH_FLAGS** se almacena en la sección de perfil Global de un perfil de la interfaz de programación de aplicaciones de mensajería (MAPI). El valor de **PR_ROH_FLAGS** es una máscara de bits que se compone de uno o varios de los siguientes indicadores. 
  
|**Nombre**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0 x 1  <br/> |Conectar con el servidor de Exchange utilizando RPC sobre HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0 x 2  <br/> |Conectar con el servidor de Exchange sólo se utiliza capa de sockets seguros (SSL).  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0 x 4  <br/> |Autenticar mutuamente la sesión al conectar con SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0 x 8  <br/> |En redes rápidas, conectar utilizando HTTP primero. A continuación, conectar utilizando TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0 x 20  <br/> |En redes lentas, conectar utilizando HTTP primero. A continuación, conectar utilizando TCP/IP.  <br/> |
   
Por ejemplo, para establecer el **PR_ROH_FLAGS** (propiedad) para activar la RPC a través de HTTP, para requerir SSL y para especificar que se debe usar en primer lugar el protocolo HTTP en conexiones lentas, establezca el valor de la propiedad **PR_ROH_FLAGS** en `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` que es igual a 0 x 23. 
  
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

