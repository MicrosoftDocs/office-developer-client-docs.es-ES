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
ms.openlocfilehash: 9d40c21cde6bf3a6e8e37dda80dd6f900f233a0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819344"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propiedad canónica PidTagContainerClass

  
  
**Hace referencia a**: Outlook 
  
Contiene una cadena de texto que describe el tipo de una carpeta. Aunque esta propiedad se omite por lo general, las versiones de Microsoft® Exchange Server antes de administrador de buzones de Exchange Server 2003 esperan que esta propiedad esté presente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificador:  <br/> |0x3613  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades no se usan normalmente por Exchange Server. Sin embargo, Microsoft Office Outlook® adjunta a las carpetas de buzón de correo. Además, las versiones de Exchange Server antes de administrador de buzones de Exchange Server 2003 incorrectamente podrían controlar las carpetas que no tengan estas propiedades.
  
Estas propiedades se pueden asignar los valores de cadena en la tabla siguiente.
  
|**Valor**|**Contenido de carpeta**|
|:-----|:-----|
|IPF. Cita  <br/> |Citas  <br/> |
|IPF. Contacto  <br/> |Contactos  <br/> |
|IPF. Diario  <br/> |Entradas de diario de Outlook  <br/> |
|IPF. Nota  <br/> |Los mensajes de correo y notas  <br/> |
|IPF. Nota rápida  <br/> |Notas rápidas de Outlook  <br/> |
|IPF. Tarea  <br/> |Tareas de Outlook  <br/> |
   
Para las carpetas que contienen los mensajes de correo, estas propiedades deben establecerse en IPF. Tenga en cuenta.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.
    
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

