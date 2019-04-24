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
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330124"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propiedad canónica PidTagResponsibility

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si algún proveedor de transporte ya ha aceptado la responsabilidad para entregar el mensaje a este destinatario y FALSE si la cola MAPI considera que este proveedor de transporte debe aceptar responsabilidad.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificador:  <br/> |0x0E0F  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando la cola MAPI presenta un mensaje saliente a un proveedor de transporte, a través de [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), establece esta propiedad en false para todos los destinatarios para los que la cola MAPI considera que el proveedor de transporte es responsable y true para todos otros destinatarios. El proveedor de transporte debería intentar controlar todos los destinatarios con **PR_RESPONSIBILITY** establecido en false. Después de enviar correctamente, o de haber fallado de forma concluyente, a un destinatario, el proveedor de transporte debe establecer esta propiedad en TRUE en el mensaje de origen para indicar que ha aceptado la responsabilidad para ese destinatario. 
  
Si después de examinar un destinatario, un proveedor de transporte decide que no puede o no debe controlarlo, el proveedor de transporte debe dejar **PR_RESPONSIBILITY** establecido en false. La cola MAPI buscará otro proveedor de transporte que pueda administrar a ese destinatario. La cola MAPI finalmente crea un informe de no entrega para todos los destinatarios para los que ningún proveedor de transporte acepta la responsabilidad. 
  
Si el proveedor de transporte intenta y no puede entregar el mensaje, debe llamar al método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para indicar a MAPI las razones del error, de modo que MAPI pueda generar un informe de no entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad can�nico de PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

