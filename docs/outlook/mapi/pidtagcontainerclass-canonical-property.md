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
  
Contiene una cadena de texto que describe el tipo de una carpeta. Aunque esta propiedad generalmente se omite, las versiones de Microsoft® Exchange Server antes de Exchange Server administrador de buzones de correo de 2003 esperan que esta propiedad esté presente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificador:  <br/> |0x3613  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades normalmente no las usa Exchange Server. Sin embargo, Microsoft Office Outlook® las adjunta a carpetas de buzones. Además, las versiones de Exchange Server antes de Exchange Server administrador de buzones de correo de 2003 podrían controlar incorrectamente carpetas que no tienen estas propiedades.
  
Estas propiedades se pueden asignar a los valores de cadena en la tabla siguiente.
  
|**Valor**|**Contenido de la carpeta**|
|:-----|:-----|
|IPF. Cita  <br/> |Citas  <br/> |
|IPF. Contacto  <br/> |Contactos  <br/> |
|IPF. Diario  <br/> |Outlook Entradas de diario  <br/> |
|IPF. Nota  <br/> |Mensajes de correo y notas  <br/> |
|IPF. StickyNote  <br/> |Outlook Notas rápidas  <br/> |
|IPF. Tarea  <br/> |Tareas de Outlook  <br/> |
   
Para las carpetas que contienen mensajes de correo, estas propiedades deben establecerse en IPF. Nota.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para crear y localizar las carpetas especiales en un buzón.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para los objetos de lista de distribución personal y de contacto.
    
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

