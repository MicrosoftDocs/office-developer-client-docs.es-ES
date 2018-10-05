---
title: Información sobre el reasignado de calendarios mediante programación para el horario de verano
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: En este tema, este período entre la primavera y otoño se conoce como el período de horario de verano.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389025"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Información sobre el reasignado de calendarios mediante programación para el horario de verano

Muchos países implementan horario de verano (horario de verano) avanzando relojes para que las tardes tengan verano más largo. Normalmente, esto se realiza estableciendo el reloj una hora con antelación en la primavera y establecer el reloj de la copia de una hora en el otoño. En este tema, este período entre la primavera y otoño se conoce como el período de horario de verano. La mayoría de países tienen su propia legislación para cuando el horario de verano comienza y termina. Las fechas del período de horario de verano pueden cambiar de un año a otro, y los usuarios deben actualizar su calendario de Microsoft Outlook cada vez que cambien las normas de horario de verano. 
  
Si utiliza una versión de Windows que es Windows Vista o posterior, o tener activa la actualización automática de Windows, puede no verse afectado por el cambio de horario de verano. De lo contrario, debe instalar las actualizaciones de horario de verano para Windows. Independientemente de si las actualizaciones se instalan automáticamente, en su nombre por un departamento de TI, o por usted mismo como un usuario particular, algunas de las citas existentes que se producen durante el período de horario de verano podrían mostrar horas incorrectas después de que se instalan las actualizaciones de horario de verano para Windows . Esto es así para las citas periódicas y de instancia única. Deberá actualizar estas citas para mostrar correctamente en Outlook, en Outlook Web App y en aplicaciones que se basan en objetos de datos de colaboración (CDO). Actualizar citas muestra incorrectamente en los calendarios a causa de horario de verano se conoce como reorganización de calendarios.
  
Outlook proporciona herramientas para los usuarios y Exchange Server proporciona herramientas para los administradores a los calendarios de reajuste. Outlook proporciona la herramienta de actualizar datos de zona horaria para los usuarios de Outlook. Con esta herramienta, los usuarios pueden actualizar sus propios calendarios. Exchange Server proporciona la herramienta de actualización de calendario de Exchange que ayuda a los administradores a fin de evitar las dificultades de resultantes de la implementación de la herramienta de Outlook ampliamente a todos los usuarios y para asegurarse de que cada usuario ejecute correctamente la herramienta de Outlook.
  
Además de basarse en los usuarios para ejecutar la herramienta de actualización de datos de zona horaria o administradores para ejecutar la herramienta de actualización de calendario de Exchange, los desarrolladores de software de cliente MAPI de terceros pueden descargar una DLL, Tzmovelib.dll. Mediante el uso de este ensamblado, los programadores pueden utilizar las mismas API que usan Outlook y Exchange Server en su calendario reorganización de herramientas. 

En la lista siguiente se muestra el calendario reajuste API:
  
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
    
Para escribir una herramienta de reajuste de cita usando el calendario reorganización de API, puede usar el siguiente procedimiento:
  
1. Use **IOlkApptRebaser::BeginEnumerateAppointments** y **IOlkApptRebaser::EndEnumerateAppointments** para buscar citas que son candidatos para modificar la base. Si es necesario, presentar información para permitir al usuario a decidir qué tipos de citas reajustar. Como alternativa, use MAPI o el modelo de objetos de Outlook para examinar la información de hora y la periodicidad de una cita mediante el análisis de la **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, y las propiedades de **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**y **IOlkApptRebaser::EndRebaseAppointments** para reajustar la cita. 
    
Para obtener el ensamblado Tzmovelib.dll, descargue el instalador del redistribuible OutlookTimeZoneMoveLibRedist.exe y el archivo de encabezado Tzmovelib.h en [Outlook 2010: instalador redistribuible de referencia auxiliar y archivo de encabezado para modificar la base de calendarios](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Esta descarga funciona para Outlook 2010 y versiones posteriores de Outlook. OutlookTimeZoneMoveLibRedist.exe instala el archivo de ensamblado Tzmovelib.dll en C:\Program Files\MsExTmz. Tenga en cuenta que las aplicaciones de reajuste de calendario de terceros pueden redistribuir a sólo el instalador, OutlookTimeZoneMoveLibRedist.exe y no deben redistribuir el ensamblado, Tzmovelib.dll o cualquier otra extrajo componentes por separado desde el programa de instalación.
  
## <a name="see-also"></a>Vea también

- [Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)
- [Horario de verano centro de ayuda y soporte técnico](https://support.microsoft.com/gp/cp_dst)
- [Cómo abordar el horario de verano con la herramienta de actualización de calendario de Exchange](https://support.microsoft.com/kb/941018)
- [Cómo abordar los cambios de zona horaria mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

