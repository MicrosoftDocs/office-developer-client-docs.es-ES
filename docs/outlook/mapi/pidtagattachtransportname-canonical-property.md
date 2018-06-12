---
title: Propiedad canónico PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819261"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propiedad canónico PidTagAttachTransportName

  
  
**Se aplica a**: Outlook 
  
Contiene el nombre de un archivo de datos adjuntos modificado para que se puede asociar con mensajes TNEF. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificador:  <br/> |0x370C  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Notas

TNEF y el proveedor de transporte usan estas propiedades. Normalmente, no están disponibles para las aplicaciones cliente. 
  
Estas propiedades se usan con frecuencia por TNEF cuando el sistema de mensajería subyacente no es compatible con los nombres de archivo proporcionado. Por ejemplo, se utilizan cuando el usuario asocia a varios archivos con el mismo nombre, como archivos de cinco denominado CONFIG. PREDETERMINADO DEL SISTEMA El proveedor de transporte debe modificar los nombres para asegurarse de que son únicos. Cada nombre modificado aparece en su adjunto **PR_ATTACH_TRANSPORT_NAME** y propiedades asociadas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

