---
title: Propiedad canónica PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2a1c49b29ba08775768fc74861ba36b3c6356fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589381"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propiedad canónica PidTagResponsibility

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si algún proveedor de transporte ya ha aceptado la responsabilidad de entregar el mensaje a este destinatario y FALSE si la cola MAPI se considera que este proveedor de transporte debe aceptar responsabilidad.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificador:  <br/> |0x0E0F  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando la cola MAPI presenta un mensaje saliente a un proveedor de transporte, a través de [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), se establece esta propiedad en FALSE para todos los destinatarios para que la cola MAPI considera ese proveedor de transporte responsable y TRUE para todas las otros destinatarios. El proveedor de transporte debe intentar controlar a todos los destinatarios con **PR_RESPONSIBILITY** establecida en FALSE. Después de enviar correctamente, o la certeza con errores enviar a un destinatario, el proveedor de transporte debe establecer esta propiedad en TRUE en el mensaje de origen para indicar que ha aceptado la responsabilidad de ese destinatario. 
  
Si, después de examinar a un destinatario, un proveedor de transporte decide que no se puede o no debería administrar, el proveedor de transporte debe dejar **PR_RESPONSIBILITY** conjunto en FALSE. Otro proveedor de transporte que puede administrar a ese destinatario, a continuación, buscará la cola de MAPI. En última instancia, la cola MAPI crea un informe de no entrega para todos los destinatarios para que ningún proveedor de transporte acepta responsabilidad. 
  
Si el proveedor de transporte intenta y no puede entregar el mensaje, debe llamar al método de [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar a MAPI las razones para el error, por lo que MAPI puede generar un informe de no entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad can�nico de PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

