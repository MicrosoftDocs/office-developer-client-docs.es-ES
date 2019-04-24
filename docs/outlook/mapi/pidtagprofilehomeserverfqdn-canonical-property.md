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
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341597"
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
|Área:  <br/> |Configuración del perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece esta propiedad en el nombre de dominio del servidor de directorio del usuario, se permite la conexión directa con el controlador de dominio (DC), que es necesario para un perfil que se ha configurado para usar la autenticación Kerberos en Microsoft Exchange Server 2007 y versiones anteriores, estableciendo **RPC_C_AUTHN_GSS_KERBEROS** en **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 y Exchange Server 2013 administran las llamadas de la libreta de direcciones que se realizan en el servidor de acceso de cliente de forma diferente a como se administran con Exchange Server 2007 y versiones anteriores. El proceso DSProxy ya no se usa, por lo que la autenticación Kerberos puede realizarse correctamente. Sin embargo, el cliente seguirá comunicándose con el servidor de Exchange en lugar de hacerlo directamente con el DC, lo cual puede no ser necesario: el establecimiento de **PR_PROFILE_HOME_SERVER_FQDN** evita esto. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica operaciones permitidas para los objetos de almacén de mensajes principales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

