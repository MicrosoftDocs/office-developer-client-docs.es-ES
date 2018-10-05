---
title: Propiedad canónica PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387499"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Propiedad canónica PidLidContactLinkSearchKey

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la lista de **SearchKeys** para el contacto vinculado a este objeto de mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidContactLinkSearchKey  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008584  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

|**Longitud en bytes**|**Descripción**|**Notas**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Ninguno  <br/> |
|variable  <br/> |Datos de SearchKey  <br/> |Repite ContactEntryCount veces  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también

- [Propiedades MAPI](mapi-properties.md) 
- [Propiedades MAPI canónicas](mapi-canonical-properties.md)
- [Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

