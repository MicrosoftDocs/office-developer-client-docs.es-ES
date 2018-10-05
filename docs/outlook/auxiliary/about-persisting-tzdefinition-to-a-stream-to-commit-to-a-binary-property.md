---
title: Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Las propiedades de la zona horaria, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur y PidLidAppointmentTimeZoneDefinitionStartDisplay son binarios denominado propiedades, cada uno de los cuales contiene una secuencia que se asigna a la formato guardado de una estructura TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398622"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria

Las propiedades de la zona horaria, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)y [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) son binarios denominado propiedades, cada uno de ellos contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](tzdefinition.md) . 
  
En este tema se describe un formato little-endian que se puede usar al almacenar **TZDEFINITION** a una secuencia de confirmación en uno de tres propiedades binarias. Utilice el mismo formato endian en un analizador para interpretar un valor de secuencia obtenido de una de estas propiedades. 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

El número de versión principal se usa para realizar cambios en una hora. Los clientes que no están familiarizados con el número de versión principal deben tratar la propiedad como si no está allí. Los clientes de escritura de la estructura deben especificar la constante **TZ_BIN_VERSION_MAJOR**. 
  
El número de versión secundaria se usa para la extensibilidad. Los clientes que no están familiarizados con el número de versión secundaria deben leer los datos que se comprenden y omitir los datos que es posible que se anexa a cada regla o a la secuencia general. Los clientes de escritura de la estructura deben especificar la constante **TZ_BIN_VERSION_MINOR**. 
  
Si un analizador de descripción de la versión principal del encabezado, no debe leer el resto de la estructura y se comportan como si los datos que faltan. Si un analizador de descripción de la versión secundaria del encabezado, que debe usar **cbHeader** para que omita la partes que no comprender y avanzada para leer las partes de la secuencia que entiende. 
  
El valor de **wFlags** siempre es **TZDEFINITION_FLAG_VALID_KEYNAME**. Nombre de la clave tiene un tamaño máximo de **MAX_PATH**. 
  
Si un analizador no reconoce la versión principal de una regla, el cliente debe omitir la regla y use **cbRule** para avanzar a la siguiente regla. Si un analizador no reconoce la versión secundaria de una regla, el cliente debe analizar sólo las partes de la regla que comprende. 
  
Cuando se almacena una estructura **TZDEFINITION** a una secuencia, un analizador no debe intentar escribir cualquier información que no comprende. 
  
El número máximo de reglas es 1024.
  
Tenga en cuenta que la estructura [TZREG](tzreg.md) se conserva aquí forma diferente de cuando se almacena por separado, por lo que el mismo código no puede usarse para analizarlo. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)

