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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341954"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propiedad canónica PidTagTnefCorrelationKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que correlaciona un archivo adjunto de formato de encapsulación neutro de transporte (TNEF) con un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificador:  <br/> |0x007F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Sobre MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los sub objetos adjuntos TNEF exponán esta propiedad. Esta propiedad determina si un archivo TNEF entrante pertenece o no al mensaje al que está adjunto. Se usa principalmente por proveedores de transporte y puertas de enlace.
  
En un mensaje saliente, el proveedor de transporte debe calcular un valor binario único para ese mensaje o usar un valor existente que satisfaga el requisito de unibilidad, como un identificador de mensaje. El proveedor de transporte debe almacenar este valor en esta propiedad y, a continuación, llamar al [método ITnef::AddProps](itnef-addprops.md) para encapsularlo. El mismo valor también debe almacenarse en el sobre de transporte en un lugar definido por el proveedor, como el encabezado del mensaje. 
  
En un mensaje entrante, el proveedor de transporte debe llamar al método [ITnef::ExtractProps](itnef-extractprops.md) para decapsular los datos adjuntos de TNEF y, a continuación, comparar esta propiedad con el valor almacenado en el sobre de transporte. Si los valores coinciden, TNEF debe procesarse normalmente, es decir, se deben usar todas las propiedades extraídas de los datos adjuntos de TNEF. Si los valores no coinciden, se deben omitir todas las propiedades de los datos adjuntos de TNEF. Si no se establece esta propiedad, se debe considerar que el archivo TNEF pertenece a este mensaje y se deben usar las demás propiedades extraídas de él. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.
    
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

