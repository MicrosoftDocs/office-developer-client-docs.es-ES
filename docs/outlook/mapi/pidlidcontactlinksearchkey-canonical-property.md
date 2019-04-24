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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319778"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Propiedad canónica PidLidContactLinkSearchKey

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la lista de **SearchKeys** del contacto al que se vincula este objeto de mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidContactLinkSearchKey  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008584  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Comentarios

|**Longitud en bytes**|**Descripción**|**Notas**|
|:-----|:-----|:-----|
|segundo  <br/> |ContactEntryCount  <br/> |Ninguno  <br/> |
|variable  <br/> |Datos de SearchKey  <br/> |RePite ContactEntryCount veces  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también

- [Propiedades MAPI](mapi-properties.md) 
- [Propiedades canónicas de MAPI](mapi-canonical-properties.md)
- [Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

