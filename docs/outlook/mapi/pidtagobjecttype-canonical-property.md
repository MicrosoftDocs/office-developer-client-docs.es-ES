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
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591054"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propiedad canónica PidTagObjectType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de un objeto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificador:  <br/> |0x0FFE  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo de objeto contenido en esta propiedad corresponde a la interfaz principal disponible para un objeto accesible a través de la interfaz de **OpenEntry** . Normalmente, se obtiene mediante el parámetro _lpulObjType_ devuelto por el método **OpenEntry** apropiado de consultoría. Cuando se obtiene la interfaz de otras maneras, llame a [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor de esta propiedad. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
MAPI_ABCONT 
  
> Objeto de contenedor de libreta de direcciones 
    
MAPI_ADDRBOOK 
  
> Objeto de la libreta de direcciones 
    
MAPI_ATTACH 
  
> Objeto de datos adjuntos del mensaje 
    
MAPI_DISTLIST 
  
> Objeto de lista de distribución 
    
MAPI_FOLDER 
  
> Objeto Folder 
    
MAPI_FORMINFO 
  
> Objeto de formulario 
    
MAPI_MAILUSER 
  
> Objeto de usuario de mensajería 
    
MAPI_MESSAGE 
  
> Objeto Message 
    
MAPI_PROFSECT 
  
> Objeto de sección de perfil 
    
MAPI_SESSION 
  
> Objeto de sesión 
    
MAPI_STATUS 
  
> Objeto de estado 
    
MAPI_STORE 
  
> Objeto de almacén de mensajes
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Administra las comunicaciones de un cliente con un servidor de la interfaz de proveedor de servicio de nombres (NSPI).
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Especifica los formatos de archivo (OAB) de la libreta de direcciones sin conexión para la caché de objetos de la libreta de direcciones locales.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

