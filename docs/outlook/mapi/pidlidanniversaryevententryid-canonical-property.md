---
title: Propiedad canónica PidLidAnniversaryEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335577"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a>Propiedad canónica PidLidAnniversaryEventEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el identificador de entrada de la cita que representa el aniversario del contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidAnniversaryEventEID  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x0000804E  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Comentarios

La cita especificada por la propiedad **dispidAnniversaryEventEID** debe estar vinculada a este contacto mediante el **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([ PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) y **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), como se detalla en [[ms-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

