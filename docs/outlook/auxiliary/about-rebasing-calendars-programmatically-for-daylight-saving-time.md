---
title: Información sobre el reasignado de calendarios mediante programación para el horario de verano
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: En este tema, este período entre el muelle y el otoño se conoce como período DST.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316959"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Información sobre el reasignado de calendarios mediante programación para el horario de verano

Muchos países observan el horario de verano (DST) marcando los relojes para que las tardes tengan más luz del día. Esto suele realizarse estableciendo el reloj una hora antes del muelle y estableciendo el reloj una hora más tarde en otoño. En este tema, este período entre el muelle y el otoño se conoce como período DST. La mayoría de los países tienen sus propias regulaciones sobre cuándo comienza y finaliza el DST. Las fechas del período de DST pueden cambiar de un año a otro, y los usuarios deben actualizar su calendario de Microsoft Outlook cada vez que cambie la normativa de DST. 
  
Si usa una versión de Windows que es Windows Vista o posterior, o tiene activada la actualización automática de Windows, es posible que no se verá afectado por el cambio en DST. De lo contrario, debes instalar las actualizaciones de DST para Windows. Independientemente de si las actualizaciones se instalan automáticamente, en su nombre por un departamento de TI o por usted mismo como usuario principal, algunas citas existentes que se producen durante el período de DST pueden mostrar horas incorrectas después de instalar las actualizaciones de DST para Windows. Esto es así tanto para citas periódicas como de instancia única. Debe actualizar estas citas para mostrarlas correctamente en Outlook, en Outlook Web App y en aplicaciones basadas en objetos de datos de colaboración (CDO). La actualización de citas mostradas incorrectamente en los calendarios debido a DST se conoce como reababamiento de calendarios.
  
Outlook proporciona herramientas para usuarios y Exchange Server proporciona herramientas para que los administradores puedan volver a base de calendarios. Outlook proporciona la herramienta de actualización de datos de zona horaria para los usuarios de Outlook. Con esta herramienta, los usuarios pueden actualizar sus propios calendarios. Exchange Server proporciona la Herramienta de actualización de calendario de Exchange que ayuda a los administradores a evitar las dificultades que se derivan de la implementación de la herramienta de Outlook ampliamente para todos los usuarios y para asegurarse de que cada usuario ejecuta la herramienta de Outlook correctamente.
  
Además de confiar en que los usuarios ejecuten la herramienta de actualización de datos de zona horaria o administradores para ejecutar la herramienta de actualización de calendario de Exchange, los desarrolladores de software cliente MAPI de terceros pueden descargar una DLL, Tzmovelib.dll. Mediante este ensamblado, los desarrolladores pueden usar las mismas API que Outlook y Exchange Server en sus herramientas de reabasado de calendario. 

En la siguiente lista se muestran las API de reabas del calendario:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Para escribir una herramienta de reabasado de citas mediante las API de reababado de calendario, puede usar el siguiente procedimiento:
  
1. Use **IOlkApptRebaser::BeginEnumerateAppointments** e **IOlkApptRebaser::EndEnumerateAppointments** para buscar citas que sean candidatas para el reabasamiento. Si es necesario, presente información para permitir que el usuario decida qué citas rebase. Como alternativa, use MAPI o el modelo de objetos de Outlook para examinar la información de tiempo y periodicidad de una cita analizando las propiedades **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** y **PidLidAppointmentTimeZoneDefinitionRecur.** 
    
2. Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** e **IOlkApptRebaser::EndRebaseAppointments** para volver a base de la cita. 
    
Para obtener el ensamblado Tzmovelib.dll, descargue el instalador redistribuible de OutlookTimeZoneMoveLibRedist.exe y el archivo de encabezado Tzmovelib.h en [Outlook 2010:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)Instalador redistribuible de referencia auxiliar y archivo de encabezado para redistribuir calendarios . Esta descarga funciona para Outlook 2010 y versiones posteriores de Outlook. OutlookTimeZoneMoveLibRedist.exe instala el archivo Tzmovelib.dll ensamblado en C:\Archivos de programa\MsExTmz. Tenga en cuenta que las aplicaciones de reasojo de calendario de terceros solo pueden redistribuir el instalador, OutlookTimeZoneMoveLibRedist.exe y no deben redistribuir el ensamblado, Tzmovelib.dll ni ningún otro componente extraído independientemente del instalador.
  
## <a name="see-also"></a>Consulte también

- [Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centro de soporte técnico y ayuda para el horario de verano](https://support.microsoft.com/gp/cp_dst)
- [Cómo solucionar el horario de verano con la Herramienta de actualización de calendario de Exchange](https://support.microsoft.com/kb/941018)
- [Cómo solucionar los cambios de zona horaria mediante la Herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

