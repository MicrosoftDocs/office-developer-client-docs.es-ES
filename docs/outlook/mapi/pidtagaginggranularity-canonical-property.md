---
title: Propiedad canónica PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325588"
---
# <a name="pidtagaginggranularity-canonical-property"></a>Propiedad canónica PidTagAgingGranularity

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa la unidad de tiempo que se usa para determinar el tiempo que un elemento permanece en una carpeta antes de archivar el elemento.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Identificador:  <br/> |0x36EE  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores posibles **PR_AGING_GRANULARITY** pueden ser uno de los siguientes. 
  
|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD** se define en número de meses.  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** se define en número de semanas.  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** se define en número de días.  <br/> |
   
El tiempo que un elemento permanece en una carpeta antes de archivar el elemento está determinado por dos propiedades, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) y **PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** representa el número de unidades de tiempo que el elemento permanece en la carpeta antes de archivarlo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicas que se usan en operaciones remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

