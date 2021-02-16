---
title: Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Las propiedades de zona horaria PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur y PidLidAppointmentTimeZoneDefinitionStartDisplay son propiedades con nombre binario, cada una de las cuales contiene una secuencia que se asigna al formato persistente de una estructura TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316980"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="6dee2-103">Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria</span><span class="sxs-lookup"><span data-stu-id="6dee2-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="6dee2-104">Las propiedades de zona horaria [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)y [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) son propiedades con nombre binario, cada una de las cuales contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION.](tzdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="6dee2-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="6dee2-105">En este tema se describe un pequeño formato endian que se puede usar al conservar **TZDEFINITION** en una secuencia para confirmar una de las tres propiedades binarias.</span><span class="sxs-lookup"><span data-stu-id="6dee2-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="6dee2-106">Usa el mismo formato endian en un analizador para interpretar un valor de secuencia obtenido de una de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6dee2-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="6dee2-107">El número de versión principal se usa para realizar un cambio importante.</span><span class="sxs-lookup"><span data-stu-id="6dee2-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="6dee2-108">Los clientes que no estén familiarizados con el número de versión principal deben tratar la propiedad como si no hubiera.</span><span class="sxs-lookup"><span data-stu-id="6dee2-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="6dee2-109">Los clientes que escriben la estructura deben especificar la **constante TZ_BIN_VERSION_MAJOR**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="6dee2-110">El número de versión secundaria se usa para la extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="6dee2-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="6dee2-111">Los clientes que no estén familiarizados con el número de versión secundaria deben leer los datos que comprendan y omitir los datos que se pueden anexar a cada regla o a la secuencia general.</span><span class="sxs-lookup"><span data-stu-id="6dee2-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="6dee2-112">Los clientes que escriben la estructura deben especificar la **constante TZ_BIN_VERSION_MINOR**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="6dee2-113">Si un analizador no comprende la versión principal del encabezado, no debe leer el resto de la estructura y comportarse como si faltasen los datos.</span><span class="sxs-lookup"><span data-stu-id="6dee2-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="6dee2-114">Si un analizador no comprende la versión secundaria del encabezado, debe usar **cbHeader** para omitir las partes que no comprende y avanzar para leer las partes de la secuencia que comprende.</span><span class="sxs-lookup"><span data-stu-id="6dee2-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="6dee2-115">El valor de **wFlags** siempre **es TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="6dee2-116">El nombre de la clave tiene un tamaño máximo de **MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="6dee2-117">Si un analizador no reconoce la versión principal de una regla, el cliente debe ignorarla y usar **cbRule** para avanzar a la siguiente regla.</span><span class="sxs-lookup"><span data-stu-id="6dee2-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="6dee2-118">Si un analizador no reconoce la versión secundaria de una regla, el cliente solo debe analizar las partes de la regla que comprende.</span><span class="sxs-lookup"><span data-stu-id="6dee2-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="6dee2-119">Al conservar una **estructura TZDEFINITION** en una secuencia, un analizador no debe intentar escribir ninguna información que no comprenda.</span><span class="sxs-lookup"><span data-stu-id="6dee2-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="6dee2-120">El número máximo de reglas es 1024.</span><span class="sxs-lookup"><span data-stu-id="6dee2-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="6dee2-121">Tenga en cuenta que la estructura [TZREG](tzreg.md) se conserva aquí de forma diferente que cuando se conserva por sí sola, por lo que no se puede usar el mismo código para analizarla.</span><span class="sxs-lookup"><span data-stu-id="6dee2-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6dee2-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6dee2-122">See also</span></span>

- [<span data-ttu-id="6dee2-123">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="6dee2-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="6dee2-124">Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6dee2-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="6dee2-125">Leer las propiedades de la zona horaria en una cita</span><span class="sxs-lookup"><span data-stu-id="6dee2-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

