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
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327450"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propiedad canónica PidTagRpcOverHttpFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la configuración de un perfil usado por Microsoft Office Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROH_FLAGS  <br/> |
|Identificador:  <br/> |0x6623  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

La **PR_ROH_FLAGS** se almacena en la sección de perfil global de un perfil de interfaz de programación de aplicaciones de mensajería (MAPI). El valor de **PR_ROH_FLAGS** es una máscara de bits que está hecha de una o varias de las siguientes marcas. 
  
|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Conéctese a la Exchange Server mediante RPC sobre HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Conéctese a la Exchange Server solo mediante capa de sockets seguros (SSL).  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Autenticar mutuamente la sesión al conectarse mediante SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |En redes rápidas, conéctese primero mediante HTTP. A continuación, conéctese mediante TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |En redes lentas, conéctese primero con HTTP. A continuación, conéctese mediante TCP/IP.  <br/> |
   
Por ejemplo, para establecer la propiedad **PR_ROH_FLAGS** para activar RPC sobre HTTP, para requerir SSL y para especificar que el protocolo HTTP debe usarse primero en conexiones lentas, establezca el valor de la propiedad PR_ROH_FLAGS que sea igual **a**  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` 0x23. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicas que se usan en operaciones remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
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

