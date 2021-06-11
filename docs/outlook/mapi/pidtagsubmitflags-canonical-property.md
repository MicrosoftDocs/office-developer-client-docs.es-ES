---
title: Propiedad canónica PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339357"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propiedad canónica PidTagSubmitFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que indica detalles sobre el envío de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificador:  <br/> |0x0E14  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Se pueden establecer una o varias de las siguientes marcas para la **máscara PR_SUBMIT_FLAGS** de bits: 
  
SUBMITFLAG_LOCKED 
  
> La cola MAPI tiene actualmente el mensaje bloqueado. 
    
SUBMITFLAG_PREPROCESS 
  
> El mensaje necesita preprocesamiento. Cuando la cola MAPI haya terminado de procesar previamente este mensaje, debe llamar al [método IMessage::SubmitMessage.](imessage-submitmessage.md) El proveedor del almacén de mensajes reconoce que el spooler, en lugar de la aplicación cliente, ha llamado **SubmitMessage**, borra la marca y continúa el envío de mensajes.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

