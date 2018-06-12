---
title: Propiedad canónico PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820032"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propiedad canónico PidTagReceiveFolderSettings

  
  
**Se aplica a**: Outlook 
  
Contiene una tabla de un mensaje almacén de configuración de la carpeta de recepción.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificador:  <br/> |0x3415  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo pt Object, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita la interfaz con el identificador de IID_IMAPITable debe tener acceso a su contenido. Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecida, pero puede, opcionalmente, identificarlo o no, si no está establecido. 
  
Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Para obtener más información, vea [Recibir carpeta tablas](receive-folder-tables.md).
  
Esta propiedad contiene una tabla de asignaciones de las carpetas de recepción para el almacén de mensajes. Al llamar a **OpenProperty** en esta propiedad es equivalente a llamar a **GetReceiveFolderTable** en el almacén de mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

