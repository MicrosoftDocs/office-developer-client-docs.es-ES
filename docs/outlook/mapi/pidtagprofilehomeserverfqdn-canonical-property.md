---
title: Propiedad canónica PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b02a55f7b87bef6a4304d006f79472bcf21c811e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581877"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Propiedad canónica PidTagProfileHomeServerFQDN

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Habilita la autenticación Kerberos de una configuración de perfil.
  
****

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Identificador:  <br/> |0x662A001F  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Configuración de perfiles de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Al establecer esta propiedad en el nombre de dominio de servidor de Active directory del usuario permite la conexión directa para el controlador de dominio (DC), que es necesario para un perfil que se ha configurado para usar la autenticación Kerberos frente a Microsoft Exchange Server 2007 y versiones anteriores, estableciendo **RPC_C_AUTHN_GSS_KERBEROS** en **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 y Exchange Server 2013 controlan las llamadas de la libreta de direcciones realizadas en el servidor de acceso de cliente de forma diferente de la manera en que Exchange Server 2007 y versiones anteriores controlan. Ya no se usa el proceso DSProxy, por lo que se puede realizar correctamente la autenticación Kerberos. Sin embargo, el cliente aún podría comunicarse con el servidor de Exchange en lugar de hacerlo directamente con el controlador de dominio, es posible que no desee: configuración **PR_PROFILE_HOME_SERVER_FQDN** evita esto. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

