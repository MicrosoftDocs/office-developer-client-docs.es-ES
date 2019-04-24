---
title: Información sobre el reasignado de calendarios mediante programación para el horario de verano
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: En este tema, este período entre el muelle y el de caída se conoce como período de DST.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316959"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Información sobre el reasignado de calendarios mediante programación para el horario de verano

Muchos países observan el horario de verano (DST) recorriendo los relojes para que las noches tengan más tiempo de horario de verano. Normalmente, esto se hace configurando el reloj una hora por delante en el muelle y estableciendo el reloj una hora hacia atrás en el caída. En este tema, este período entre el muelle y el de caída se conoce como período de DST. La mayoría de los países tienen su propia reglamentación para cuando se inicia y finaliza el horario de verano. Las fechas del período de DST pueden cambiar de un año a otro y los usuarios deben actualizar su calendario de Microsoft Outlook cada vez que cambien las regulaciones de DST. 
  
Si usa una versión de Windows que sea Windows Vista o posterior, o si tiene activada la actualización automática de Windows, es posible que no se vea afectado por el cambio en el horario de verano. De lo contrario, debe instalar las actualizaciones de DST para Windows. Independientemente de si las actualizaciones se instalan automáticamente, en su nombre por un departamento de ti o como un usuario doméstico, algunas citas existentes que se producen durante el período del DST pueden mostrar horas incorrectas después de instalar las actualizaciones de DST para Windows. . Esto se aplica tanto a las citas periódicas como a las de instancia única. Debe actualizar estas citas para que se muestren correctamente en Outlook, en Outlook Web App y en aplicaciones basadas en objetos de datos de colaboración (CDO). La actualización incorrecta de las citas en los calendarios debido al horario de verano se conoce como reajuste de calendarios.
  
Outlook proporciona herramientas para los usuarios y Exchange Server, que proporciona herramientas para que los administradores rebasen los calendarios. Outlook proporciona la herramienta de actualizar datos de zona horaria para los usuarios de Outlook. Con esta herramienta, los usuarios pueden actualizar sus propios calendarios. Exchange Server proporciona la herramienta de actualización de calendario de Exchange, que ayuda a los administradores a evitar dificultades que resultan de la implementación generalizada de la herramienta de Outlook para todos los usuarios y para asegurarse de que cada usuario ejecuta la herramienta de Outlook correctamente.
  
Además de confiar en que los usuarios ejecuten la herramienta de actualizar datos de zona horaria o los administradores para ejecutar la herramienta de actualización de calendario de Exchange, los programadores de software de cliente MAPI de terceros pueden descargar una DLL, Tzmovelib. dll. Mediante este ensamblado, los desarrolladores pueden usar las mismas API que Outlook y Exchange Server usan en sus herramientas de reajuste de calendario. 

En la siguiente lista se muestran las API de reajuste del calendario:
  
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
    
Para escribir una herramienta de reajuste de citas mediante las API de reajuste del calendario, puede usar el siguiente procedimiento:
  
1. Use **IOlkApptRebaser:: BeginEnumerateAppointments** y **IOlkApptRebaser:: EndEnumerateAppointments** para buscar citas que sean candidatas para el reajuste. Si es necesario, presente información que permita al usuario decidir qué citas se deben rebasar. Como alternativa, use MAPI o el modelo de objetos de Outlook para examinar la información de tiempo y periodicidad de una cita analizando el **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** y propiedades de **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Use **HrCreateApptRebaser**, **IOlkApptRebaser:: BeginRebaseAppointments**y **IOlkApptRebaser:: EndRebaseAppointments** para rebasar la cita. 
    
Para obtener el ensamblado Tzmovelib. dll, descargue el instalador redistribuible de OutlookTimeZoneMoveLibRedist. exe y el archivo de encabezado Tzmovelib. h en [Outlook 2010: archivo de encabezado y instalador redistribuible de referencia auxiliar para](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) reajustar calendarios . Esta descarga funciona para Outlook 2010 y versiones posteriores de Outlook. OutlookTimeZoneMoveLibRedist. exe instala el archivo de ensamblado Tzmovelib. dll en C:\Program Files\MsExTmz. Tenga en cuenta que el calendario de terceros el reajuste de aplicaciones puede redistribuir solo el instalador, OutlookTimeZoneMoveLibRedist. exe, y no debe redistribuir el ensamblado, Tzmovelib. dll, ni ningún otro componente extraído por separado del instalador.
  
## <a name="see-also"></a>Vea también

- [Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centro de ayuda y soporte técnico del horario de verano](https://support.microsoft.com/gp/cp_dst)
- [Cómo dirigir el horario de verano mediante la herramienta de actualización de calendario de Exchange](https://support.microsoft.com/kb/941018)
- [Cómo dirigir los cambios de zona horaria mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

