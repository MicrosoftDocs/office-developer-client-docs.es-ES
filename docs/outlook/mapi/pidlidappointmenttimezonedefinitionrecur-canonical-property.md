---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345356"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se crea una cita periódica o una convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefRecur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008260  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Las versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en objetos de datos de colaboración (CDO) 1.2.1 que ejecutan la herramienta de actualización de calendario de Outlook o Exchange Server usan la **dispidApptTZDefRecur** y ** **propiedades de dispidTimeZoneStruct ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar si la reunión periódica debe ajustarse si las reglas de la zona horaria cambian. Estas propiedades deben estar sincronizadas, ya que los clientes más antiguos pueden seguir manipulando la propiedad **dispidTimeZoneStruct** . Para detectar si las dos propiedades están sincronizadas, el miembro **wFlags** de la regla que coincide con **dispidTimeZoneStruct** debe tener establecida la marca TZRULE_FLAG_RECUR_CURRENT_TZREG. Si no se establece esta marca, o se establece, y la regla de la propiedad **dispidTimeZoneStruct** no coincide con la regla marcada, debe descartarse la propiedad **dispidApptTZDefRecur** y se debe usar **dispidTimeZoneStruct** en su lugar. 
  
Cuando se escriben las propiedades **dispidApptTZDefRecur** y **dispidTimeZoneStruct** en una nueva reunión periódica, o cuando se realiza una opción arbitraria para usar la propiedad **dispidTimeZoneStruct** , la definición actual de la zona horaria ( según el registro de Windows) debe usarse. 
  
Un analizador debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefRecur**o cuando continúa **TZDEFINITION** en una secuencia para que se comprometa a una propiedad binaria como **dispidApptTZDefRecur**. Para obtener más información, vea [acerca de la persistencia de TZDEFINITION en una secuencia para confirmar una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** especifica la información de zona horaria que describe cómo convertir la fecha y hora de la reunión en una serie periódica a y desde la hora universal coordinada (UTC). Si se establece esta propiedad pero tiene datos que no son coherentes con los datos representados por **dispidTimeZoneStruct**, el cliente debe usar **dispidTimeZoneStruct** en lugar de **dispidApptTZDefRecur**. Si no se establece **dispidApptTZDefRecur** , se usará la propiedad **PidLidTimeZoneStruct** en su lugar. Los campos de este BLOB se codifican en el orden de bytes Little-Endian. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

