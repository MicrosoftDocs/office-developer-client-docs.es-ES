---
title: Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Las propiedades de zona horaria, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur y PidLidAppointmentTimeZoneDefinitionStartDisplay son propiedades con nombre binario, cada una de las cuales contiene una secuencia que se asigna al formato persistente de una estructura TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316980"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria

Las propiedades de zona horaria, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)y [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) son propiedades con nombre binario, cada una de las cuales contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION.](tzdefinition.md) 
  
En este tema se describe un pequeño formato endian que se puede usar al conservar **TZDEFINITION** en una secuencia para confirmar una de las tres propiedades binarias. Use el mismo formato endian en un analizador para interpretar un valor de secuencia obtenido de una de estas propiedades. 
  
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

El número de versión principal se usa para realizar un cambio de última hora. Los clientes que no estén familiarizados con el número de versión principal deben tratar la propiedad como si no está ahí. Los clientes que escriben la estructura deben especificar la **constante TZ_BIN_VERSION_MAJOR**. 
  
El número de versión secundaria se usa para la extensibilidad. Los clientes que no estén familiarizados con el número de versión secundaria deben leer los datos que comprendan y omitir los datos que se pueden anexar a cada regla o a la secuencia general. Los clientes que escriben la estructura deben especificar la **constante TZ_BIN_VERSION_MINOR**. 
  
Si un analizador no comprende la versión principal del encabezado, no debe leer el resto de la estructura y comportarse como si faltasen los datos. Si un analizador no entiende la versión secundaria del encabezado, debe usar **cbHeader** para ignorar las partes que no comprende y avanzar para leer las partes de la secuencia que comprende. 
  
El valor de **wFlags** siempre **es TZDEFINITION_FLAG_VALID_KEYNAME**. El nombre de clave tiene un tamaño máximo de **MAX_PATH**. 
  
Si un analizador no reconoce la versión principal de una regla, el cliente debe omitir la regla y usar **cbRule** para avanzar a la siguiente regla. Si un analizador no reconoce la versión secundaria de una regla, el cliente solo debe analizar las partes de la regla que comprende. 
  
Al conservar una **estructura TZDEFINITION** en una secuencia, un analizador no debe intentar escribir ninguna información que no comprenda. 
  
El número máximo de reglas es 1024.
  
Tenga en cuenta que [la estructura TZREG](tzreg.md) persiste aquí de forma diferente que cuando se conserva solo, por lo que no se puede usar el mismo código para analizarla. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)

