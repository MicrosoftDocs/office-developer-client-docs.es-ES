---
title: Propiedad canónica PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386421"
---
# <a name="pidtagdisplayname-canonical-property"></a>Propiedad canónica PidTagDisplayName

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre para mostrar para un determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x3001  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Las carpetas requieren las subcarpetas del mismo nivel que los nombres de presentación únicos. Por ejemplo, si una carpeta contiene dos subcarpetas, las dos subcarpetas no pueden usar el mismo valor de esta propiedad. Esta restricción no se aplica a otros contenedores, como libretas de direcciones y listas de distribución. 
  
Proveedores de servicios deben establecer el valor de esta propiedad para que contenga tanto la información de configuración y tipo de proveedor. La información adicional ayuda a distinguir entre instancias de los proveedores del mismo tipo. Sin configurar proveedores deben usar una cadena que asigna el proveedor. Configurado los proveedores deben usar la misma cadena seguida de una cadena distintiva entre paréntesis. Por ejemplo, un proveedor de almacén de mensajes no configurado puede establecer estas propiedades: 
  
Almacén de información personal
  
La versión configurada, a continuación, puede establecer estas propiedades: 
  
Almacén de información personal (6 de febrero de 1998)
  
Para los objetos de estado, estas propiedades contienen el nombre del componente que se puede mostrar la interfaz de usuario. 
  
> [!NOTE]
> Punto y coma no se puede usar dentro de nombres de los destinatarios de mensajería MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Extiende el protocolo WebDAV que especifica cómo solicitar y establecer el descriptor de seguridad de Exchange a través de los métodos de WebDAV.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

