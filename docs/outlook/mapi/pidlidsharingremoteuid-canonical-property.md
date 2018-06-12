---
title: Propiedad canónico PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cb8b4a7c71f3ad81949f3eac6cab230f40c6d487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818924"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>Propiedad canónico PidLidSharingRemoteUid

  
  
**Se aplica a**: Outlook 
  
Especifica el identificador de entrada de la carpeta remota que se está compartiendo. Esto es una propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingRemoteUid  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008A06  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Uso compartido  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad debe establecerse en la representación de cadena hexadecimal del valor de la propiedad de entrada del objeto ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la carpeta que se está compartida. Esto es una propiedad de un mensaje para compartir.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte las carpetas de buzón de correo entre los clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

