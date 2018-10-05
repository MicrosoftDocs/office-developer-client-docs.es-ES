---
title: Propiedad canónica PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393848"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propiedad canónica PidTagTnefCorrelationKey

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que correlaciona un dato adjunto de formato de encapsulación neutro de transporte (TNEF) con un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificador:  <br/> |0x007F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Sobres MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los objetos secundarios de los datos adjuntos TNEF exponen esta propiedad. Esta propiedad determina si un archivo TNEF entrante pertenece al mensaje que está unido. Se utiliza principalmente por proveedores de transporte y las puertas de enlace.
  
En un mensaje saliente, el proveedor de transporte debe calcular un valor binario único a ese mensaje, o usar un valor existente que cumple el requisito de unicidad, como un identificador de mensaje. El proveedor de transporte debe almacenar este valor en esta propiedad y, a continuación, llamar al método [ITnef::AddProps](itnef-addprops.md) para encapsularlo. El valor de la misma también debe almacenarse en el contenedor de transporte en un lugar definido por el proveedor, por ejemplo, el encabezado del mensaje. 
  
En un mensaje entrante, el proveedor de transporte debe llamar al método [ITnef::ExtractProps](itnef-extractprops.md) para los datos adjuntos TNEF desencapsulan y, a continuación, compare esta propiedad con el valor almacenado en el contenedor de transporte. Si los valores coinciden, se debe procesar TNEF normalmente, es decir, se deben usar todas las propiedades extraídas de los datos adjuntos TNEF. Si los valores no coinciden, se deben omitir todas las propiedades de los datos adjuntos TNEF. Si no se establece esta propiedad, se debe considerar el archivo TNEF que pertenecen a este mensaje, y las demás propiedades extraídas de los deben usarse. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
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

