---
title: Propiedad canónica PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283152"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propiedad canónica PidTagContainerClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena de texto que describe el tipo de una carpeta. Aunque esta propiedad suele omitirse, las versiones de Microsoft ® Exchange Server anteriores a Exchange Server 2003 el administrador de buzones esperan que esta propiedad esté presente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificador:  <br/> |0x3613  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Normalmente, Exchange Server no usa estas propiedades. Sin embargo, Microsoft Office Outlook ® las adjunta a las carpetas del buzón. Además, las versiones de Exchange Server anteriores a Exchange Server 2003 el administrador de buzones podrían tratar incorrectamente las carpetas que no tienen estas propiedades.
  
A estas propiedades se les pueden asignar los valores de cadena de la tabla siguiente.
  
|**Value**|**Contenido de la carpeta**|
|:-----|:-----|
|Error. Convoca  <br/> |Citas  <br/> |
|Error. Contact  <br/> |Contactos  <br/> |
|Error. Agenda  <br/> |Entradas del diario de Outlook  <br/> |
|Error. Note  <br/> |Notas y mensajes de correo  <br/> |
|Error. StickyNote  <br/> |Notas rápidas de Outlook  <br/> |
|Error. Tareas  <br/> |Tareas de Outlook  <br/> |
   
Para las carpetas que contienen mensajes de correo, estas propiedades deben establecerse en IPF. Note.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de contacto y de lista de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

