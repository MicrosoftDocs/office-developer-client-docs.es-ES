---
title: Propiedad canónica PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391181"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propiedad canónica PidTagAgingPeriod

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Representa el número de unidades de tiempo que se usan para determinar el período de tiempo que permanece un producto en una carpeta antes de que se archiva el elemento.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AGING_PERIOD  <br/> |
|Identificador:  <br/> |0x36EC  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

El período de tiempo que permanece un producto en una carpeta antes de que se archiva el elemento se determina mediante dos propiedades, **PR_AGING_PERIOD** y **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** representa la unidad de tiempo en que se expresa **PR_AGING_PERIOD** , al determinar este período de tiempo. 
  
Los valores posibles para **PR_AGING_GRANULARITY** pueden ser una de las siguientes opciones. 
  
****

|**Nombre**|**Descripción**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** se define en el número de meses.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** se define en el número de semanas.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** se define en el número de días.  <br/> |
   
Por ejemplo, si un archivos de carpeta es un elemento sólo después de que el elemento ha sido en la carpeta para dos semanas y, a continuación, **PR_AGING_GRANULARITY** **AG_WEEKS** y **PR_AGING_PERIOD** es 2. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicos que se usan en las operaciones remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

