---
title: Propiedad canónica PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329228"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propiedad canónica PidTagObjectType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de objeto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificador:  <br/> |0x0FFE  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Común  <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo de objeto contenido en esta propiedad corresponde a la interfaz principal disponible para un objeto accesible a través de la **interfaz OpenEntry.** Normalmente se obtiene consultando el parámetro  _lpulObjType_ devuelto por el método **OpenEntry** adecuado. Cuando la interfaz se obtiene de otras maneras, llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor de esta propiedad. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
MAPI_ABCONT 
  
> Objeto contenedor de libreta de direcciones 
    
MAPI_ADDRBOOK 
  
> Objeto libreta de direcciones 
    
MAPI_ATTACH 
  
> Objeto de datos adjuntos de mensaje 
    
MAPI_DISTLIST 
  
> Objeto de lista de distribución 
    
MAPI_FOLDER 
  
> Objeto Folder 
    
MAPI_FORMINFO 
  
> Form (objeto) 
    
MAPI_MAILUSER 
  
> Objeto de usuario de mensajería 
    
MAPI_MESSAGE 
  
> Objeto Message 
    
MAPI_PROFSECT 
  
> Objeto de sección Perfil 
    
MAPI_SESSION 
  
> Session (objeto) 
    
MAPI_STATUS 
  
> Status (objeto) 
    
MAPI_STORE 
  
> Objeto de almacén de mensajes
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Controla las comunicaciones de un cliente con un servidor de interfaz de proveedor de servicios de nombres (NSPI).
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Especifica los formatos de archivo de libreta de direcciones sin conexión (OAB) para la memoria caché de objetos de libreta de direcciones local.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

