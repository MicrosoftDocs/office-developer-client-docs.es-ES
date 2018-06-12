---
title: Propiedad canónico PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cba8de706e7262ff59abdb6367fb505a2303dcf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820063"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a>Propiedad canónico PidTagRemindersOnlineEntryId

  
  
**Se aplica a**: Outlook 
  
Contiene la **propiedad EntryID** de la carpeta de avisos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REM_ONLINE_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D5  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes. Para obtener acceso a la propiedad en un almacén de mensajes específicos, siga este procedimiento. 
  
1. En primer lugar, busque la propiedad en la carpeta Bandeja de entrada. Utilice [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obtener una referencia a la **propiedad EntryID** de la carpeta Bandeja de entrada. 
    
2. Si **IMsgStore::GetReceiveFolder** se realiza correctamente, a continuación, usar la referencia a la **propiedad EntryID** de la Bandeja de entrada y [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** . 
    
3. Si **IMsgStore::OpenEntry** se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener la propiedad deseada. 
    
4. Si se produce un error en el paso 1, 2 o 3, busque la propiedad en la carpeta raíz. Para ello, use **IMsgStore::OpenEntry**, especificar NULL para **lpEntryID**, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** . 
    
5. Si abrir la carpeta raíz se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad que desee. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
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

