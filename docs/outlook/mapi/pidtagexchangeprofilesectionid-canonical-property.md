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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699516"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propiedad canónica PidTagExchangeProfileSectionId

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un GUID generado de forma dinámica se utiliza para determinar una cuenta cuando esté usando varias cuentas de Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificador:  <br/> |0x3d150102  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Varias cuentas de Exchange  <br/> |
   
## <a name="remarks"></a>Observaciones

Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten varias cuentas de Exchange en lugar de una única cuenta de Exchange. Para dar cabida a varias cuentas de Exchange, se ha cambiado el diseño de perfiles MAPI. En Microsoft Office Outlook 2007 y versiones anteriores, los perfiles contiene una sección de perfil fijo dedicada a la configuración de Exchange, como el nombre del servidor, el nombre de usuario y el archivo de carpetas sin conexión (.ost). ubicación. Estas opciones se han identificado mediante el uso de un identificador único, la propiedad **pbGlobalProfileSectionGuid** . La sección que se usa para la configuración de Exchange se denomina la sección de perfil Global de Exchange. 
  
Una ubicación de sección de perfil fijo ya no es suficiente para dar cabida a varias cuentas de Exchange. En su lugar, para cada cuenta de Exchange en su perfil, existe una sección dedicada a la configuración para esa cuenta. La nueva sección usada para la configuración de Exchange se identifica mediante el identificador único **emsmdbUID**.
  
En la sección de perfil de servicio de mensaje para la cuenta de Exchange, puede encontrar una propiedad que contiene un GUID que se genera de forma dinámica en el momento en que se crea la cuenta. Este GUID se almacena en la propiedad **PidTagExchangeProfileSectionId** . Almacenes de mensajes y los contenedores de la libreta de direcciones exponen una propiedad para determinar qué cuenta de Exchange que pertenecen. Puede tener acceso en la tabla de servicios de mensaje, cada servicio de Exchange expone esta propiedad. 
  
Puede recuperar esta propiedad a través de una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) en **PidTagExchangeProfileSectionId** después de la consulta de cualquiera de las siguientes interfaces: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si el objeto no está relacionado con Exchange, la llamada devuelve **MAPI_E_NOT_FOUND**.
  
Puede restringir los contenedores en un **PidTagExchangeProfileSectionId** al mostrar la libreta de direcciones. Una vez que haya un contenedor abierto, puede consultar el **emsmdbUID** de él. También merece la pena tener en cuenta que si se ha seleccionado un destinatario de una libreta de direcciones de Exchange, el destinatario también tiene la **PidTagExchangeProfileSectionId** en su lista de propiedades. 
  
> [!NOTE]
> A lo largo de los ejemplos de código y los encabezados de función, este GUID se conoce como **emsmdbUID**. 
  
Una de las cuentas de Exchange está marcada como la cuenta de Exchange heredada. Normalmente, es la primera cuenta que se agregan al perfil. Todas las llamadas para abrir **pbGlobalProfileSectionGuid** se redirigen a la sección global de Exchange de la cuenta heredada. Las llamadas al modelo de objeto que interactúan con la cuenta de Exchange heredado que no sean también interactúan con la cuenta de Exchange heredada. 
  
El servicio de Exchange heredado tiene la propiedad **PR_EMSMDB_LEGACY** (0x3D18000B), que se establece en **true** en la tabla de servicios de mensaje. 
  
El heredado **emsmdbUID** también se mostrará en la sección de perfil de Outlook Global del perfil como **PidTagExchangeProfileSectionId**. El código escrito para admitir varias cuentas de Exchange no debe tener que recuperar el heredado **emsmdbUID** debido a que debe obtener la correcta **emsmdbUID**, dependiendo de la cuenta de con que su código está interactuando.
  
## <a name="see-also"></a>Consulte también



[Uso de varias cuentas de Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

