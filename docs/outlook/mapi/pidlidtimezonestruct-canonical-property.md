---
title: Propiedad canónica PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346378"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propiedad canónica PidLidTimeZoneStruct

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , que describe la zona horaria que se va a usar para la hora de inicio y finalización de una cita periódica o una convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTimeZoneStruct  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008233  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Office Outlook 2003, versiones anteriores de Outlook y aplicaciones basadas en objetos de datos de colaboración (CDO) 1,21 cuyos usuarios no han ejecutado la herramienta de actualización de calendario proporcionada por Outlook o Exchange Server almacene la hora de inicio y la hora de finalización de un cita periódica o convocatoria de reunión como hora relativa y almacene la zona horaria donde se crea la cita o la convocatoria de reunión en **dispidTimeZoneStruct**. Sin embargo, esta combinación no tiene en cuenta que, con el tiempo, las reglas de zona horaria pueden cambiar, lo que da lugar a citas y reuniones que los usuarios programados antes de que las reglas cambien y se produzcan en momentos incorrectos. Los usuarios y administradores que no ejecutan Windows Vista o que no tienen activadas las actualizaciones automáticas deben usar las herramientas de reajuste del calendario que proporcionan Outlook o Exchange Server para ajustar el tiempo de dichas citas y convocatorias de reunión. Para obtener más información sobre estas herramientas de reajuste del calendario y las API que reorganizan los calendarios, vea [acerca del reajuste de calendarios mediante programación para el horario de verano](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Use el siguiente formato Little-Endian al analizar una secuencia obtenida de **dispidTimeZoneStruct**, o al conservar la estructura **TZREG** en una secuencia para confirmar la propiedad binaria **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Esta propiedad se establece en una serie periódica para especificar la información de zona horaria y especifica cómo convertir los campos de tiempo entre la hora local y la hora universal coordinada (UTC).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

