---
title: Propiedad canónica PidTagReceiveFolderSettings
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356745"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propiedad canónica PidTagReceiveFolderSettings

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla de la configuración de la carpeta de recepción de un almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificador:  <br/> |0x3415  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo PT Object, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente; debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , que solicita la interfaz con el identificador IID_IMAPITable. Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido. 
  
Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Para obtener más información, vea [Receive Folder tables](receive-folder-tables.md).
  
Esta propiedad contiene una tabla de asignaciones de las carpetas de recepción del almacén de mensajes. Llamar a **OpenProperty** en esta propiedad equivale a llamar a **GetReceiveFolderTable** en el almacén de mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

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

