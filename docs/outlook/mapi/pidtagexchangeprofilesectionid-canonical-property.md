---
title: Propiedad canónica PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316432"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propiedad canónica PidTagExchangeProfileSectionId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un GUID generado dinámicamente que se usa para determinar una cuenta cuando se usan varias Microsoft Exchange Server cuentas.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificador:  <br/> |0x3d150102  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Varias cuentas de Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten varias Exchange en lugar de una sola Exchange cuenta. Para dar cabida a varias Exchange, se cambió el diseño del perfil MAPI. En Microsoft Office Outlook 2007 y versiones anteriores, los perfiles contenían una sección de perfil fijo dedicada a la configuración de Exchange, como el nombre del servidor, el nombre de usuario y el archivo de carpeta sin conexión (.ost). ubicación. Esta configuración se identificó mediante un identificador único, la **propiedad pbGlobalProfileSectionGuid.** La sección usada para la Exchange se denomina Exchange de perfil global. 
  
Una ubicación de sección de perfil fijo ya no es suficiente para dar cabida a varias Exchange cuentas. En su lugar, para Exchange cuenta del perfil, existe una sección dedicada a la configuración de esa cuenta. La nueva sección usada para la Exchange se identifica mediante el identificador único **emsmdbUID**.
  
En la sección perfil de servicio de mensajes de la cuenta Exchange, puede encontrar una propiedad que contenga un GUID que se genera dinámicamente en el momento en que se crea la cuenta. Este GUID se almacena en la **propiedad PidTagExchangeProfileSectionId.** Los almacenes de mensajes y los contenedores de libreta de direcciones exponen una propiedad para determinar Exchange cuenta a la que pertenecen. Accesible en la tabla de servicios de mensajes, Exchange servicio expone esta propiedad. 
  
Puede recuperar esta propiedad mediante una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) en **PidTagExchangeProfileSectionId** después de consultar cualquiera de las interfaces siguientes: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si el objeto no está asociado con Exchange, la llamada devuelve **MAPI_E_NOT_FOUND**.
  
Puede restringir contenedores en **un PidTagExchangeProfileSectionId** al mostrar la libreta de direcciones. Una vez que tenga un contenedor abierto, puede consultar **el emsmdbUID** desde él. También es importante tener en cuenta que si un destinatario se seleccionó de una libreta de direcciones de Exchange, el destinatario también tiene **pidTagExchangeProfileSectionId** en su lista de propiedades. 
  
> [!NOTE]
> A lo largo de los ejemplos de código y los encabezados de función, este GUID se conoce como **emsmdbUID**. 
  
Una de las Exchange cuenta está marcada como cuenta heredada Exchange cuenta. Normalmente, es la primera cuenta agregada al perfil. Cada llamada para abrir **pbGlobalProfileSectionGuid** se redirige a la Exchange global de la cuenta heredada. Las llamadas del modelo de objetos que interactúan con la cuenta de Exchange no heredada también interactúan con la cuenta Exchange heredada. 
  
El servicio de Exchange heredado tiene la propiedad **PR_EMSMDB_LEGACY** (0x3D18000B), que se establece en **true** en la tabla de servicios de mensajes. 
  
El **emsmdbUID** heredado también se marca en la sección Outlook perfil global del perfil como **PidTagExchangeProfileSectionId**. El código escrito para admitir varias cuentas de Exchange no debe tener que recuperar el **emsmdbUID** heredado porque debe obtener el **emsmdbUID** correcto, en función de la cuenta con la que interactúe el código.
  
## <a name="see-also"></a>Vea también



[Uso de varias Exchange cuentas](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

