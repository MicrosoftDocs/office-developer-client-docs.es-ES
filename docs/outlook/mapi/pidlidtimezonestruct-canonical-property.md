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
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819000"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propiedad canónica PidLidTimeZoneStruct

  
  
**Hace referencia a**: Outlook 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) , que se describe la zona horaria que se usará para la hora de inicio y finalización de una cita periódica o convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTimeZoneStruct  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008233  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Office Outlook 2003, las versiones anteriores de Outlook y las aplicaciones que se basan en Collaboration Data Objects (CDO) 1.21 cuyos usuarios no se ejecuta la herramienta de actualización de calendario proporcionada por Outlook o Exchange Server almacenan la hora de inicio y hora de finalización de un periódica una cita o convocatoria de reunión como tiempo relativo y almacenar la zona horaria donde se crea la solicitud de reunión o cita en **dispidTimeZoneStruct**. Sin embargo, este esquema omite que con el tiempo, las reglas de zona horaria pueden cambiar, resultante en algunas citas y reuniones que los usuarios programado antes de que las reglas ha cambiado y se produzcan en momentos incorrectas. Los usuarios y administradores que no ejecutan Windows Vista o que no tienen actualizaciones automáticas está activada deben usar el calendario reorganización de las herramientas proporcionadas por Outlook o Exchange Server para ajustar el tiempo de dichas citas y convocatorias de reunión. Para obtener más información acerca de estas herramientas de reajuste de calendario y las API que reorganización de calendarios, vea [acerca de los calendarios reajuste mediante programación del horario de verano](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Use el siguiente formato "little-endian" al analizar una secuencia obtenida desde **dispidTimeZoneStruct**, o cuando se almacena la estructura **TZREG** a una secuencia para confirmar a la propiedad binarios **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Esta propiedad se establece en una serie periódica para especificar la información de zona horaria y especifica cómo se convierten los campos de tiempo entre la hora local y la hora Universal coordinada (UTC).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

